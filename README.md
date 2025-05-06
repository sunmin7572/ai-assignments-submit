# ai-assignments-submit

# 1. 가상환경 생성
python3 -m venv myenv
source myenv/bin/activate  # Windows는 venv\Scripts\activate

# 2. 필수 도구 설치
pip install pip-tools

# 3. 패키지 설치
pip-compile requirements.in
pip install -r requirements.txt
pip install notebook
pip install ipykernel

# 4. 주피터 노트북 커널에 가상환경 등록
python -m ipykernel install --user --name=myenv --display-name "Python (myenv)"

# 5. 주피터 노트북 실행
jupyter notebook
ai_assignments_note.ipynb 오픈
Python(myenv) 커널에서 코드 실행

# 6. 최종 결과물
qat_model_Base-CE_int8.onnx
qat_model_Base-Focal_int8.onnx
qat_model_Adapter-CE_int8.onnx
qat_model_Adapter-Focal_int8.onnx
