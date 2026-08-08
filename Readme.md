# [Yandex] Agents Week [RUS, 2026]

<br/>

https://shad.yandex.ru/agentsweek

https://www.youtube.com/watch?v=C1OCgbONSAw&list=PL6Wui14DvQPzSfe9EfQhlanlIHaj70GQc

<br/>

**Халява закончилась. GitHub отключил возможность бесплатно пользоваться gpt-4o-mini:**  
https://github.com/marketplace/models

<br/>

DeepSeek-R1 - Request included unsupported tool use. Using tool is not supported by this model

Llama-3.3-70B-Instruct - Request included unsupported tool use. This model does not support more than one tool call at this time

<br/>

```python
from langchain_openai import ChatOpenAI

os.environ["MY_API_KEY"] = "sk-or-v1-"

MODEL_NAME = "openrouter/free"
MODEL_API_BASE="https://openrouter.ai/api/v1"

llm = ChatOpenAI(
    model=MODEL_NAME,
    temperature=0.2,
    openai_api_key=os.environ["MY_API_KEY"],
    openai_api_base=MODEL_API_BASE,
)

# try:
#     response = llm.invoke("Привет! Ты работаешь?")
#     print("Ответ модели:", response.content)
# except Exception as e:
#     print("Произошла ошибка при подключении:", e)
```

<br/>

```python
os.environ["MY_API_KEY"] = "github_pat_***"
MODEL_NAME = "Llama-3.3-70B-Instruct"
MODEL_API_BASE="https://models.github.ai/inference"

llm = ChatOpenAI(
    model=MODEL_NAME,
    temperature=0,
    openai_api_key=os.environ["MY_API_KEY"],
    openai_api_base=MODEL_API_BASE,
)
```

<br/>

### Лекция 1.1 Intro to AI Agents LLM

```
00:01 Приветствие и задачи AI-службы в Яндекславке
03:21 Обзор программы интенсива по AI-агентам
05:33 Темы текущего занятия: применение и теория
06:12 Примеры использования AI-агентов в бизнесе
07:21 Эволюция взаимодействия: от промптинга до систем
09:15 Различные определения AI-агента в индустрии
10:13 Структура агента: модель, промпты, инструменты, память
12:35 Аналогия LLM как новой операционной системы
13:30 Физическая суть LLM: веса и код
14:50 Обучение моделей и Next Token Prediction
16:05 Токенизация и специальные токены управления
20:08 Контекстное окно и параметры генерации (температура)
21:44 Три этапа обучения: Pre-training, Fine-tuning, RLHF
23:55 Природа галлюцинаций и способы борьбы с ними
24:47 Сильные и слабые стороны LLM на практике
26:30 Практика: локальный инференс против API
32:00 Демонстрация галлюцинаций в коде
33:55 Ограничения: арифметика, подсчет символов и свежие знания
35:35 Введение в бенчмарк Tau Bench для оценки агентов
37:40 Разработка базового агента авиакомпании на LangGraph
41:30 Архитектура LangChain и LangGraph для продакшена
43:10 Сборка первого графа и тестирование ответов
44:40 Анонс следующего занятия: инструменты и MCP
```

<br/>

### Лекция 1.2 Tools. MCP

https://agentskills.io/home

<br/>

### Лекция 2 Memory and Guardrails in LLM-Powered Agents

<br/>

### Лекция 3 AI Agent Workflow Multi-Agent Systems Multimodality

<br/>

### Лекция 4 Agent Evaluation: From Metrics to Managed Quality

```
00:01 Введение и план практической части
01:37 Настройка инфраструктуры и простейшего агента
03:50 Сбор траектории работы агента
06:05 Тестовый запуск и анализ логов
07:08 Формирование корзины задач (тестового датасета)
09:35 Генерация дополнительных задач с помощью LLM
11:01 Типы грейдеров: детерминированный и политический
13:32 Реализация «железного пользователя» для симуляции
17:01 Определение неявных критериев: Usefulness, Groundness, Efficiency
18:13 Создание Gold Standard (ручная разметка)
19:46 Разработка и итеративное улучшение LLM-судьи
22:15 Анализ ошибок первой версии судьи
24:22 Улучшение судьи: критерии и Chain-of-Thought
28:56 Использование Few-shot примеров в промптах
31:05 Переход на более сильную модель (GPT-4)
31:40 Итоговое сравнение версий в скорборде
32:30 Визуализация прогресса и анализ метрики Каппа
34:01 Итоги практики и выводы по созданию агентов
35:10 Чек-лист по построению системы оценки (Eval)
39:02 Связь Eval-системы с производственным циклом
```

<br/>

### Лекция 5.1 Production Engineering for LLM Agents

<br/>

### Лекция 5.2 Production Engineering for LLM Agents
