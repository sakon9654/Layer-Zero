# ทำงานร่วมกับ Codex GitHub

- Source project: novel B
- Conversation ID: `6aae1f51-3c9c-83ec-9f21-cdf7029575ea`
- Imported as reference; statements here are not automatically Canon.

## ผู้เขียน

อยากทำงานร่วมกับ codex ที่ควรอ่านไฟล์อแหล่งข้อมูลจำนวนมากจาก git

## ChatGPT

ถ้าต้องการใช้ **ChatGPT + Codex + GitHub เพื่อเขียนนิยายเรื่องนี้ร่วมกันในระยะยาว** ผมแนะนำให้เปลี่ยนจากการเก็บข้อมูลทั้งหมดไว้ในแหล่งข้อมูลของ Project มาเป็นการใช้ GitHub Repository เป็นคลังข้อมูลหลักของจักรวาลนิยาย (Source of Truth)

โดยเฉพาะเรื่อง *โลกชั้นที่ศูนย์* ที่เรากำลังสร้าง เพราะในอนาคตจะมีทั้ง World Setting, Organization Setting, ประวัติตัวละคร, แฟ้ม Deviation, Timeline และเนื้อหานิยายจำนวนมาก

## 1. โครงสร้าง GitHub ที่แนะนำ

ตั้ง Repository ชื่อประมาณ `layer-zero-novel`

```text
layer-zero-novel/
│
├── AGENTS.md
│
├── README.md
│
├── canon/
│   ├── world/
│   │   ├── layer-zero.md
│   │   ├── the-deep.md
│   │   └── deviation.md
│   │
│   ├── organizations/
│   │   └── the-office.md
│   │
│   ├── characters/
│   │   ├── non.md
│   │   └── supporting-characters.md
│   │
│   ├── anomalies/
│   │   ├── entities/
│   │   │   ├── E-003.md
│   │   │   └── E-017.md
│   │   │
│   │   ├── objects/
│   │   │   ├── O-044.md
│   │   │   └── O-108.md
│   │   │
│   │   ├── phenomena/
│   │   └── locations/
│   │
│   └── timeline/
│       └── master-timeline.md
│
├── story/
│   ├── arcs/
│   │   ├── arc-01/
│   │   │   ├── outline.md
│   │   │   ├── chapter-001.md
│   │   │   └── chapter-002.md
│   │   │
│   │   └── arc-02/
│   │
│   └── master-outline.md
│
├── planning/
│   ├── mysteries.md
│   ├── foreshadowing.md
│   └── unresolved-questions.md
│
└── archive/
    └── deprecated-canon/
```

ข้อดีคือ Codex สามารถอ่านข้อมูลเฉพาะส่วนที่เกี่ยวข้องกับงานได้ ไม่จำเป็นต้องโหลดนิยายทั้งหมดทุกครั้ง

---

## 2. AGENTS.md สำคัญมาก

ไฟล์นี้จะเป็นคำสั่งหลักสำหรับ Codex เมื่อทำงานใน Repository

ตัวอย่างสำหรับโปรเจกต์นี้:

```markdown
# Layer Zero Novel — Writing Instructions

You are assisting with the development of a supernatural
mystery novel set in the Layer Zero universe.

## Canon Rules

All files under /canon are authoritative.

Before writing or modifying story content:

1. Read relevant world-setting documents.
2. Read relevant character profiles.
3. Read relevant anomaly files.
4. Check the master timeline.
5. Check existing chapters for continuity.

Never silently contradict established canon.

If a contradiction is discovered, report it before
making changes.

## Writing Style

The novel combines:

- Mystery
- Investigation
- Supernatural Horror
- Cosmic Horror
- Bureaucratic Horror
- Action and Survival

Maintain a grounded contemporary setting.

Supernatural phenomena should have observable patterns,
but their complete nature may remain unknown.

Avoid introducing conventional magic systems.

## Character Continuity

Characters must retain established personalities,
knowledge, motivations, and limitations.

Do not reveal hidden character information prematurely.

## Canon Changes

Do not modify established canon without explicit
authorization from the author.

New information introduced in chapters should be
reported as potential canon additions.

## Language

Write novel prose in Thai.

Use established English terminology for
organizations, classifications, and anomalies
where appropriate.
```

---

## 3. วิธีทำงานร่วมกันระหว่างคุณ ChatGPT และ Codex

ผมแนะนำให้แบ่งหน้าที่ดังนี้

| เครื่องมือ | หน้าที่ |
|---|---|
| คุณ | ผู้กำหนดทิศทางและตัดสินใจเรื่อง Canon |
| ChatGPT | พัฒนาเนื้อเรื่อง ตัวละคร ปริศนา และบทสนทนา |
| Codex | อ่าน Repository ตรวจสอบความต่อเนื่อง แก้ไขและจัดการไฟล์ |
| GitHub | เก็บ Canon และประวัติการเปลี่ยนแปลง |

ตัวอย่างการทำงาน:

**ขั้นแรก:** เราคุยกันใน ChatGPT เพื่อออกแบบ Arc 1

**ขั้นที่สอง:** ให้ Codex อ่าน Canon ทั้งหมดที่เกี่ยวข้อง แล้วสร้างไฟล์ Outline ของ Arc 1

**ขั้นที่สาม:** ให้ Codex ตรวจสอบว่าพล็อตที่สร้างขัดกับข้อมูลเดิมหรือไม่

**ขั้นที่สี่:** เมื่อคุณอนุมัติ จึงเริ่มเขียน Chapter 1

**ขั้นที่ห้า:** เมื่อเขียนจบแต่ละบท ให้ Codex ตรวจสอบว่ามีข้อมูลใหม่ใดที่ควรบันทึกลง Canon

วิธีนี้จะช่วยลดปัญหาที่ AI เขียนนิยายยาว ๆ แล้วลืมรายละเอียดที่เคยกำหนดไว้

---

## 4. เรื่องสำคัญ: Codex ไม่จำเป็นต้องอ่านทุกไฟล์ทุกครั้ง

สมมติในอนาคต Repository มีเอกสาร 500 ไฟล์ และนิยาย 200 บท

การสั่งให้ Codex อ่านทุกอย่างก่อนเขียนหนึ่งบทจะสิ้นเปลือง Context มาก

ควรมีไฟล์ `canon/INDEX.md` ทำหน้าที่เป็นสารบัญจักรวาลนิยาย

ตัวอย่าง:

```markdown
# Canon Index

## World
- world/layer-zero.md
- world/the-deep.md
- world/deviation.md

## Main Characters
- characters/non.md

## Organizations
- organizations/the-office.md

## Important Entities
- anomalies/entities/E-003.md
- anomalies/entities/E-017.md

## Important Objects
- anomalies/objects/O-044.md
- anomalies/objects/O-108.md

## Current Story Arc
- ../story/arcs/arc-01/outline.md
```

จากนั้นกำหนดให้ Codex อ่านสารบัญก่อน แล้วเลือกอ่านเอกสารที่เกี่ยวข้องกับงาน

สำหรับงานตรวจสอบความต่อเนื่องทั้งเรื่อง ค่อยให้ Codex ตรวจสอบ Repository ในวงกว้าง

---

## 5. สามารถเชื่อม GitHub เข้ากับ ChatGPT ได้ด้วย

หากเชื่อม GitHub คุณสามารถให้ผมช่วยทำงานกับ Repository โดยตรงได้ เช่น ค้นหาไฟล์ Canon ที่เกี่ยวข้องกับนนท์ อ่านประวัติ Entity หรือช่วยตรวจสอบความขัดแย้งระหว่างข้อมูลตัวละครกับบทนิยาย

การเชื่อมต่อ GitHub จะช่วยให้เราไม่ต้องคัดลอกเอกสารจำนวนมากกลับมาใส่แหล่งข้อมูลของ Project ทุกครั้ง

### สิ่งที่ผมแนะนำให้ทำต่อ

สำหรับโปรเจกต์ *โลกชั้นที่ศูนย์* เรามี World Setting และ Organization Setting อยู่แล้ว ขั้นต่อไปควรจัดทำ **Novel Knowledge Base** ที่ออกแบบมาเพื่อให้ทั้ง ChatGPT และ Codex ใช้งานร่วมกันโดยเฉพาะ

จุดสำคัญที่สุดคือแยกข้อมูลออกเป็นสามประเภท:

- **Established Canon:** ข้อเท็จจริงที่คุณกำหนดแล้วและห้าม AI เปลี่ยนเอง
- **Hidden Canon:** ความจริงเบื้องหลังที่ผู้เขียนรู้ แต่ตัวละครและผู้อ่านยังไม่รู้
- **In-Universe Knowledge:** สิ่งที่สำนักงานหรือตัวละครเชื่อ ซึ่งอาจเป็นข้อมูลผิดพลาดได้

การแยกสามประเภทนี้สำคัญกับนิยายแนว Cosmic Horror มาก เพราะ **สิ่งที่สำนักงานบันทึกว่าเป็นความจริง ไม่จำเป็นต้องเป็นความจริงของจักรวาลนิยาย**

