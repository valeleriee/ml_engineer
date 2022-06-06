# ml_engineer
## О задаче и желаемом результате

Решаемая задача — это прикладная задача информационной безопасности в области анализа текста (лингвистика).
Исходная постановка задачи: сбор, описание и аналитика угроз по реальным документам — довольно широка и предполагает достаточную свободу действий.

Результатом может быть программа, ML-модель, иная реализация, которая позволит решать прикладные задачи сбора и анализа неструктурированных данных об угрозах в области информационной безопасности.

# Зачем и почему?
В качестве входных данных мы предлагаем использовать датасет аналитических threat intelligence-отчетов за период с 2007 по 2020 год, сконвертированный в формат *.txt. Небольшая часть датасета предварительно размечена.

Отчеты исследователей — прекрасный по качеству источник данных TI. Отчеты содержат в себе профильтрованные и проанализированные специалистами выводы, причинно-следственные связи, наименования вредоносных кампаний, вредоносного ПО, группировок, индикаторы компрометации и взаимосвязи этих сущностей, которые имеют немалую ценность для аналитиков, занимающихся реагированием на инциденты.

# Структура репозитория
APT_CyberCriminal_Campaign_Collections — исходные сырые данные, из которых был получен датасет в *.txt. Присутствует в репозитории исключительно for reference.

converted — рабочий датасет TI-отчетов, предлагаемый для выполнения задания. Датасет представляет собой структуру директорий, разбитую по годам, в каждой директории лежат файлы *.txt. То есть, для обработки всех *.txt нужно рекурсивно обойти все директории от корневой директории набора данных (датасета).

marked — размеченная часть датасета.

Из текста удобно выделять именованные объекты и присваивать этим объектам теги. Ниже перечислены примеры объектов (сущностей), которые могут встречаться в наборе данных (датасете), а также примеры источников, где можно найти справочники этих объектов (сущностей) — это лишь примеры, вероятно в сети Интернет можно найти более полные примеры.

## Уязвимости [CVE]
https://nvd.nist.gov/vuln
## Дефекты разработки [CWE]
https://cwe.mitre.org
## Уязвимое ПО [SOFTWARE]
https://nvd.nist.gov/products/cpe
## Вредоносное ПО [MALWARE]
https://malpedia.caad.fkie.fraunhofer.de/families
https://github.com/mitre/cti/tree/master/enterprise-attack/malware
https://raw.githubusercontent.com/mitre-attack/attack-website/master/data/stix/enterprise-attack.json
https://docs.oasis-open.org/cti/stix/v2.1/cs01/stix-v2.1-cs01.html#_oxlc4df65spl
https://github.com/MISP/misp-galaxy/tree/main/clusters
## Получение планов действий [COURSE_OF_ACTION]
https://github.com/mitre/cti/tree/master/enterprise-attack/course-of-action
https://github.com/mitre/cti/tree/master/capec/course-of-action
## Наборы для проникновения [INTRUSION_SET]
https://github.com/mitre/cti/blob/master/enterprise-attack/intrusion-set/intrusion-set--fd19bd82-1b14-49a1-a176-6cdc46b8a826.json
## Вредоносные группировки [THREAT_ACTOR]
https://malpedia.caad.fkie.fraunhofer.de/actors
https://attack.mitre.org/groups
## Инструменты [TOOL]
https://github.com/mitre/cti/tree/master/enterprise-attack/tool
## Паттерны атак [ATTACK_PATTERN]
https://github.com/mitre/cti/tree/master/enterprise-attack/attack-pattern
https://github.com/mitre/cti/tree/master/capec/attack-pattern
https://docs.oasis-open.org/cti/stix/v2.1/cs01/stix-v2.1-cs01.html#_k2b7lkt45f0i
## Индустрии [INDUSTRY]
https://docs.oasis-open.org/cti/stix/v2.1/cs01/stix-v2.1-cs01.html#_oogrswk3onck
https://github.com/MISP/misp-galaxy/blob/main/clusters/sector.json
## MITRE техники и сабтехники (в первую очередь, ENTERPRISE) [MITRE_ATTACK]
https://attack.mitre.org
https://raw.githubusercontent.com/mitre/cti/master/enterprise-attack/enterprise-attack.json
## Вредоносные кампании [CAMPAIGN]
https://oasis-open.github.io/cti-documentation/examples/defining-campaign-ta-is.html
## Наименования организаций [ORG]
## Наименования стран [COUNTRY]
## Наименования городов [CITY]
## Геолокацию [GEOLOCATION]
## Временные метки (даты, время) [TIMESTAMP]
## Индикаторы компрометации [IOC] — опционально, так как есть множество нюансов и corner-cases
ipv4
ipv6
domain
url
registry key
md5
sha1
sha256
sha512
ssdeep
email
## Иные (по возможности)
STIX™ Vocabularies: https://docs.oasis-open.org/cti/stix/v2.1/cs01/stix-v2.1-cs01.html#_izngjy1g98l2
https://github.com/MISP/misp-galaxy

## Методики, вайтпейперы
https://www.microsoft.com/security/blog/2019/08/08/from-unstructured-data-to-actionable-intelligence-using-machine-learning-for-threat-intelligence/
https://github.com/jivoi/awesome-ml-for-cybersecurity
https://habr.com/ru/post/516098/
https://t.me/natural_language_processing/23530
https://habr.com/ru/post/530878/
## Референсы
Примеры выделенных объектов и их атрибутов из датасета вы можете посмотреть в директории ./ner_examples

