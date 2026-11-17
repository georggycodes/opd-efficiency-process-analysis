# Improving Outpatient Department Efficiency Through Data-Driven Process Analysis

**Independent portfolio case study | Hospital Process Analysis | November 2026**  
**Author:** Adedoyin George

> An illustrative outpatient department (OPD) process-analysis project using **250 synthetic encounter records** to examine patient flow, waiting times and departmental performance, and to develop evidence-led process-improvement hypotheses.

---

## Project overview

Outpatient care involves multiple connected stages, from arrival and registration through nursing assessment, medical consultation and, where required, laboratory and pharmacy services. Delays at one stage can extend the overall patient journey and may contribute to downstream queues.

This project uses a simulated OPD dataset covering **1–28 September 2026** for an illustrative outpatient setting in Abuja, Nigeria. The data was analysed using Microsoft Excel and Power BI to measure key process intervals, compare performance across four departments and identify patterns that warrant further operational investigation.

The project is an **independent learning and portfolio exercise**. It is not based on an actual hospital engagement, and no real patient records were used.

## Project objectives

- Measure waiting and service durations across the main outpatient process stages.
- Compare encounter volume, waiting time and total journey duration across four departments.
- Examine arrival-hour patterns associated with longer consultation waits.
- Identify operational patterns that merit root-cause investigation.
- Develop testable process-improvement hypotheses and a measurement framework.
- Demonstrate how data analysis and visual reporting can support operational decision-making.

## Tools and skills demonstrated

| Tool / capability | Application in this project |
|---|---|
| **Microsoft Excel** | Encounter-level data review, field and data-type checks, KPI verification and exploratory analysis. |
| **Power BI Desktop** | Data modelling, measures, interactive report pages, slicers and departmental comparisons. |
| **DAX** | Distinct encounter counts, average-duration measures and filtered measures for optional services. |
| **Process analysis** | Patient-flow assessment, stage-based waiting-time analysis, time-of-day analysis and departmental comparison. |
| **Improvement planning** | Root-cause hypotheses, evidence requirements, prioritised workstreams, pilot roadmap and performance measures. |

## Dataset and scope

| Attribute | Description |
|---|---|
| Dataset | 250 synthetic OPD encounter records |
| Period | 1–28 September 2026 |
| Setting | Illustrative OPD in Abuja, Nigeria |
| Departments | General Medicine; Obstetrics & Gynaecology; Paediatrics; Surgery |
| Visit types | Scheduled appointments and walk-ins |
| Optional services | Laboratory required for 118 encounters; pharmacy required for 181 encounters |
| Primary analysis table | `OPD_Data` |

`Encounter_ID` identifies an encounter, not a unique person. The analysis therefore counts **encounters**, not distinct individuals across possible repeat visits.

### Modelled patient pathway

**Arrival → Registration → Nursing assessment → Doctor consultation → Laboratory (if required) → Pharmacy (if required) → Departure**

Laboratory and pharmacy stages are optional; their duration measures use only encounters for which the relevant service was required.

## Power BI dashboard

The report contains three pages, each addressing a different operational question.

### 1. Executive Overview

Summarises overall encounter volume, patient journey, consultation and registration waiting times, satisfaction, department distribution and appointment status.

![Executive Overview dashboard](02_PowerBI_Dashboard/Dashboard_Screenshots/page-1-executive-overview.png)

### 2. Patient Flow & Waiting-Time Analysis

Examines waiting time across registration, nursing and consultation; consultation waiting by arrival hour; laboratory turnaround; and pharmacy total time.

![Patient Flow and Waiting-Time Analysis dashboard](02_PowerBI_Dashboard/Dashboard_Screenshots/page-2-patient-flow-analysis.png)

### 3. Departmental Performance Analysis

Compares encounter volume, average patient journey and satisfaction across the four departments, supported by a departmental KPI scorecard.

![Departmental Performance dashboard](02_PowerBI_Dashboard/Dashboard_Screenshots/page-3-departmental-performance.png)

## Key findings

The following are **descriptive results from the synthetic dataset**, not verified hospital performance measures.

### Overall process indicators

| Indicator | Result | Measurement note |
|---|---:|---|
| Total OPD encounters | **250** | Encounter records, not unique people |
| Average patient journey | **151.9 min** | Arrival to recorded departure |
| Average registration wait | **18.2 min** | Arrival to registration start |
| Average nursing wait | **9.5 min** | Registration completion to nursing assessment start |
| Average consultation wait | **36.6 min** | Nursing assessment end to consultation start |
| Average laboratory turnaround | **43.0 min** | **n = 118**; laboratory service start to result readiness; excludes pre-service queue |
| Average pharmacy total time | **19.3 min** | **n = 181**; pharmacy arrival to exit; includes waiting and dispensing |
| Average satisfaction indicator | **4.36 / 5** | Simulated indicator, not an independent patient survey |

### Arrival-hour pattern

- **141 of 250 encounters (56.4%)** arrived between 08:00 and 10:59.
- Average consultation waiting time peaked at **09:00 at 46.0 minutes**.
- The 08:00 and 09:00 groups each contained 49 encounters, with average consultation waits of 40.2 and 46.0 minutes respectively.

This makes the morning period a priority for investigation. Arrival concentration alone does not establish the cause; clinician availability, appointment mix, case mix and workflow conditions would need to be examined using real operational evidence.

### Departmental comparison

| Department | Encounters | Share | Consultation wait | Patient journey | Satisfaction |
|---|---:|---:|---:|---:|---:|
| General Medicine | 105 | 42.0% | 35.3 min | 149.8 min | 4.38 / 5 |
| Obstetrics & Gynaecology | 56 | 22.4% | 41.4 min | 154.7 min | 4.34 / 5 |
| Paediatrics | 53 | 21.2% | 34.5 min | 150.5 min | 4.43 / 5 |
| Surgery | 36 | 14.4% | 36.3 min | 155.6 min | 4.25 / 5 |

Additional optional-service observations:

- General Medicine had the highest departmental laboratory turnaround average: **47.3 minutes (n = 48 lab-required encounters)**.
- Paediatrics had the highest departmental pharmacy total-time average: **20.8 minutes (n = 41 pharmacy-required encounters)**.

Departmental averages are descriptive. They are not adjusted for clinical acuity, complexity, appointment type or service mix and should not be interpreted as a league table.

## Operational interpretation and improvement priorities

The analysis points to areas for **further investigation**, not proven root causes. The proposed priorities are:

1. **Consultation-flow efficiency:** map the post-nursing queue; compare hourly arrivals with clinician availability; investigate handovers, interruptions and consultation-room utilisation.
2. **Morning demand and capacity alignment:** analyse scheduled and walk-in arrivals by hour; compare demand with actual staffing and service capacity; test staggered appointment slots only where evidence supports them.
3. **Obstetrics & Gynaecology consultation pathway:** examine visit type, urgency, provider coverage, room availability and department-specific workflow.
4. **General Medicine laboratory workflow:** separate pre-service laboratory queue time from processing turnaround; examine test mix, sample transport, verification and equipment records.
5. **Paediatrics pharmacy workflow:** capture dispensing-start time and investigate prescription complexity, clarification, workload and arrival peaks.

### Proposed 90-day roadmap

| Phase | Timing | Main activities | Deliverable |
|---|---|---|---|
| Validate and map | Days 1–30 | Obtain approval; validate real records and timestamp definitions; map the process; observe peak periods; establish a baseline and local service standards. | Validated baseline and prioritised root-cause report |
| Pilot selected changes | Days 31–60 | Select one or two validated interventions; co-design with staff; test in a defined area or shift; monitor outcome and balancing measures. | Pilot protocol and interim performance report |
| Evaluate and scale | Days 61–90 | Compare with baseline; review staff and patient feedback; assess unintended effects; standardise, adapt or stop interventions. | Evaluation report and scale-up recommendation |

### Measures for evaluating improvement

Potential measures include mean, median and 90th-percentile consultation wait; percentage of encounters within locally approved waiting-time standards; waiting time by arrival hour and department; separate laboratory queue and turnaround times; pharmacy queue and dispensing times (once dispensing-start time is collected); total patient journey; patient feedback; and balancing measures such as errors, rework, complaints, overtime and patients leaving before completion.

Targets should be set only after a real hospital baseline and locally approved standards have been established. No efficiency gain or intervention impact is claimed in this project.

## Limitations and responsible interpretation

- All 250 encounter records are **synthetic** and are not representative of a real hospital or patient population.
- The 28-day period may not capture seasonal, weekly or longer-term variation.
- Staffing and room-count fields are illustrative, not a verified roster or capacity record.
- Laboratory turnaround excludes the queue before laboratory service begins.
- Pharmacy time combines waiting and dispensing because a dispensing-start timestamp is not available.
- Satisfaction is simulated and partly linked to journey duration; it is not independent evidence of patient experience.
- Departmental averages are not adjusted for acuity, clinical complexity or service mix.
- The analysis identifies patterns and investigation priorities; it does not establish causation.

Clinical leaders retain responsibility for clinical prioritisation and care decisions. The role of the analyst is to support process measurement, evidence review and operational improvement.

## Project files

| File | Description |
|---|---|
| [Portfolio Case Study (PDF)](01_Project_Documentation/Portfolio_Case_Study.pdf) | Main written case study and proposed improvement plan |
| [Editable Case Study (Word)](01_Project_Documentation/Portfolio_Case_Study.docx) | Editable version of the written report |
| [Power BI Dashboard (PDF)](02_PowerBI_Dashboard/OPD_Dashboard.pdf) | Three-page dashboard export |
| [Synthetic OPD Dataset (Excel)](03_Dataset/Synthetic_OPD_Dataset.xlsx) | Encounter-level synthetic data and supporting worksheets |

## Repository structure

```text
.
├── README.md
├── 01_Project_Documentation/
│   ├── Portfolio_Case_Study.pdf
│   └── Portfolio_Case_Study.docx
├── 02_PowerBI_Dashboard/
│   ├── OPD_Dashboard.pdf
│   └── Dashboard_Screenshots/
│       ├── page-1-executive-overview.png
│       ├── page-2-patient-flow-analysis.png
│       └── page-3-departmental-performance.png
└── 03_Dataset/
    └── Synthetic_OPD_Dataset.xlsx
```

## Professional relevance

This independent project demonstrates transferable capabilities relevant to Hospital Process Analyst roles:

- Operational KPI definition and analysis.
- Data-quality checks and encounter-level analysis.
- Trend, time-of-day and departmental comparisons.
- Power BI dashboard development and performance reporting.
- Process investigation and root-cause hypothesis development.
- Improvement planning, pilot measurement and balancing indicators.

The work demonstrates analytical methods and proposed improvement planning. It does **not** claim prior hospital employment, an actual hospital client engagement or a completed operational intervention.

---

**Author:** Adedoyin George  
**Project type:** Independent portfolio case study  
**Data status:** Synthetic / simulated  
**Analysis period:** 1–28 September 2026
