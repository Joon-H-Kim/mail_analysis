# mail_analysis
Real-Time Organizational Email Network Analyzer

본 프로젝트는 Apache Kafka, Apache Spark, 그래프 머신러닝(Graph ML)을 사용해 이메일 데이터를 분석하여 조직 내 숨겨진 협업 구조를 탐색하고 시각화하는 도구입니다.

🚀 프로젝트 개요

목표: 조직 내 비공식 네트워크 구조를 자동으로 분석 및 시각화하여, 잠재적 협업 기회 및 비공식 리더를 추천합니다.

주요 기술: Kafka, Spark Structured Streaming, GraphFrames, Node2Vec, FastAPI

🛠 주요 구성 요소

구성요소

설명

Kafka

이메일 데이터 실시간 스트리밍 처리

Apache Spark

데이터 처리 및 ETL 파이프라인

Graph ML(Node2Vec)

비공식 네트워크 구조 및 협업 임베딩 생성

FastAPI

추천 시스템 REST API 제공

React + D3.js

네트워크 그래프 및 협업 구조 시각화

📂 디렉토리 구조

.
├── data/
│   └── raw_data/
├── kafka/
│   └── producer_enron.py
├── spark/
│   ├── streaming_pipeline.py
│   └── graph_analysis.py
├── graph_ml/
│   └── node2vec_embedding.ipynb
├── api/
│   └── main.py
└── frontend/
    ├── package.json
    └── src/

⚙️ 시작 방법

1. 환경 설정

# 환경 설정
pip install -r requirements.txt

2. Kafka 스트리밍 실행

# 이메일 데이터 스트리밍
python kafka/producer_enron.py --input_dir data/raw_data --bootstrap localhost:9092 --topic emails_raw

3. Spark 스트리밍 분석

# Spark ETL & 그래프 분석
spark-submit spark/streaming_pipeline.py

4. API 서버 실행

# FastAPI 서버 실행
uvicorn api.main:app --reload

5. 프론트엔드 실행

cd frontend
npm install
npm start

🧪 기능 및 활용 예시

조직 내 비공식 리더 및 협업 그룹 자동 식별

협업 네트워크 및 의사소통 패턴 실시간 시각화

특정 직원에 대한 협업 추천
