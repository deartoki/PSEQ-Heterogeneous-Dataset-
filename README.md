This repository provides the **data crawling scripts, preprocessing pipeline, and heterogeneous graph construction workflow**
for building a **public-safety-oriented heterogeneous graph dataset (PSEQ-style)** used in the paper:

**A Fusion Model to Cognize the Structure of Heterogeneous Graph for Public Safety Scenarios**

---

## ⚠️ Important Notice
Since the dataset construction is closely related to our **ongoing project**,  
some key construction details and the final processed dataset will be **progressively released in later stages**.

At this stage, the repository provides:

- The raw data collected via our web crawler, which serves as the original source for public-safety event analysis.
- The heterogeneous graph construction workflow, including data preprocessing, node/edge definition, and graph schema design.

This repository supports the **reproducibility of the dataset construction methodology**,  
but **does NOT provide the final processed dataset**.

---

## 1. Dataset Objective

The goal is to construct a **PSEQ-style heterogeneous graph** from social media data, where:

- Each post corresponds to a public safety incident  
- Nodes represent topics, post content, users, and event categories  
- Edges capture semantic, behavioral, and contextual relationships  

---

## 2. Event Category Design

A PSEQ-style dataset includes **four major public safety domains**:

- Network Security  
- Food Safety  
- Travel Safety  
- Pharmaceutical Safety  

These domains cover a wide range of incidents and form the macro-level category structure.

---

## 3. Fine-Grained Event Types

Within the four domains, the dataset can include **ten typical event types**, such as:

1. Loan Scams  
2. Train Station Scams  
3. Travel Scams  
4. Food Poisoning  
5. Fake Order Scams  
6. Overpriced Miracle Drugs  
7. Pit-Fermented Sauerkraut  
8. Scented Rice Fraud  
9. Transfer Scams  
10. Customer Service Scams  

Researchers may customize event types based on specific needs.

---

## 4. Node Types in the Heterogeneous Graph

The PSEQ-style graph includes **four major node types**:

### **(1) Topic Indicator Nodes (T)**
Represent topic attention levels derived from expert knowledge or topic modeling.

### **(2) Blog Detail Nodes (D)**
Represent the discussion intensity of public safety incidents, extracted from post content.

### **(3) MicroBlog & Blogger Nodes (M)**
Contain user and post attributes, such as:
- Posting tool  
- Release time  
- Location  
- Hashtags  
- Behavioral features  

### **(4) Event Category Nodes**
There are four main categories, including network security, food safety, travel safety, and pharmaceutical safety.
