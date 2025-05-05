# Initial structure for the open source project `zk-identity-verifier`

# 📁 Root of the repository
README.md
LICENSE
.gitignore
docker-compose.yml
requirements.txt

# 📁 backend/
main.py  # API using Flask/FastAPI to handle uploads and processing
utils/
  - ocr.py            # OCR using Tesseract or Google Vision
  - face_match.py     # Face matching between document and live capture
  - liveness.py       # Liveness detection for video selfies
  - validation.py     # Document validation rules
models/
  - insightface/
  - facenet/
  - liveness_model/

# 📁 zk_module/
generate_proof.py   # Generates ZK proof for validated attributes
circuits/
  - age_verification.circom
  - gender_check.circom

# 📁 formats/
# YAML files describing national ID document layouts
PT_national_id.yaml
FR_passport.yaml
US_driver_license.yaml

# 📁 training_data/
# Synthetic training/testing documents
images/
labels/
scripts/

# 📁 validation_tests/
test_cases/
  - PT_id_test1.jpg
  - PT_id_test2_fake.jpg
expected_results.json

# 📁 contrib/
add_new_format_template.yaml
HOW_TO_CONTRIBUTE.md
scripts/
  - format_checker.py

# 📁 frontend/
ReactApp/  # Capture video, upload ID, display results
