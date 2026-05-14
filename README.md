

# Merkle-Rooted Blockchain and Pedersen Commitment-Based Credit Risk Assessment


This repository contains the implementation of a secure and interpretable financial credit risk assessment framework. The framework combines machine learning, HMAC-SHA256 record hashing, Merkle-tree verification, permissioned blockchain auditability, Pedersen commitment-based proof-of-knowledge, verified inference, and explainable AI.

The main goal of this project is to build a tamper-evident and privacy-aware credit-risk pipeline where credit records are verified before being passed to the machine learning model.

---
## Authors
Monirul Islam Mahmud*, Shivam Patel*, Mohamed Rahouti (Member, IEEE), Abdellah Chehri (Senior Member, IEEE) and Kaiqi Xiong (Senior Member, IEEE)

---
## Author Affiliations

Monirul Islam Mahmud, Shivam Patel, and Mohamed Rahouti are with the Department of Computer and Information Science, Fordham University, New York, NY, 10023, USA.  

Abdellah Chehri is with the Department of Mathematics and Computer Science, Royal Military College of Canada (RMC), Kingston, Ontario, Canada.  

Kaiqi Xiong is with Cyber Florida, University of South Florida, Tampa, FL, 33620, USA.  

---

## Dataset 
Credit Risk Dataset - https://www.kaggle.com/datasets/laotse/credit-risk-dataset 

## Main Features

- Credit-risk prediction using multiple machine learning models
- SMOTE-based class balancing for imbalanced credit data
- HMAC-SHA256 hashing of canonicalized raw credit records
- Merkle-tree construction for efficient record-level integrity verification
- Permissioned blockchain storage of Merkle roots and audit metadata
- Applicant-level indexing and record versioning
- Pedersen commitment-based proof-of-knowledge with Merkle-record transcript binding
- Verified vs. unverified inference comparison
- SHAP and LIME explanations for model interpretability
- Runtime, storage, and verification overhead analysis

---

## Framework Overview

The framework follows five main steps:

1. **Data Preparation and ML Training**
   - Load and preprocess credit-risk data
   - Encode categorical attributes
   - Scale numerical features
   - Apply SMOTE only on the training set
   - Train and compare multiple ML classifiers

2. **HMAC-Based Record Hashing and Merkle Batching**
   - Convert each raw credit record into a canonical format
   - Compute a per-record HMAC-SHA256 hash
   - Use the record HMAC as the Merkle-tree leaf
   - Build Merkle trees over batches of records

3. **Permissioned Blockchain Audit Layer**
   - Store only the Merkle root and audit metadata on-chain
   - Keep raw credit records off-chain
   - Maintain applicant index information, including block index, leaf position, record HMAC, and version metadata

4. **Pedersen Commitment-Based Verification**
   - Commit to a selected credit attribute using Pedersen commitments
   - Generate a proof-of-knowledge transcript
   - Bind the proof transcript to the Merkle root, record HMAC, and applicant ID
   - Apply the threshold condition as a system-level eligibility gate

5. **Verified Inference and Explainability**
   - Verify Merkle inclusion before inference
   - Verify the Pedersen transcript
   - Pass only accepted records to the ML model
   - Generate SHAP and LIME explanations for prediction transparency

---


## Citation

If you use this repository, please cite the related manuscript:

```bibtex
@article{mahmud2026merkle,
  title={Tamper-Evident Credit-Risk Assessment via Privacy-Aware Blockchain Verification and Explainable AI},
  author={Mahmud, Monirul Islam and Patel, Shivam and Rahouti, Mohamed and Chehri, Abdellah and Xiong, Kaiqi},
  journal={IEEE Transactions on Information Forensics and Security},
  year={2026}
}
```

---

## Figures

<img width="2730" height="1536" alt="fig1" src="https://github.com/user-attachments/assets/d4b4e98b-d0b2-48f0-a5e2-801c4f1373c0" />

<img width="30640" height="15421" alt="fig18" src="https://github.com/user-attachments/assets/e13336fa-c07e-4f49-8566-298c1e7ee4b0" />

<img width="6435" height="3485" alt="fig19" src="https://github.com/user-attachments/assets/6de2a26d-927f-48b4-a5f7-25a08148ace4" />
