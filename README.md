# YOLO-Small-Model (YOLO26 Nano)

Lightweight version of YOLO26 Vision App — **all tasks use nano models (~6MB)** for speed and low memory. Upload an image/video and get **detection, segmentation, classification and pose** in one web UI. Served on **port 8000**.

### Why Nano?
- `yolo26n.pt` = 6MB vs `yolo26s.pt` = 22MB vs `yolo26m.pt` = 80MB
- 3x faster inference, runs on CPU, perfect for edge devices
- Default models: `yolo26n.pt`, `yolo26n-seg.pt`, `yolo26n-cls.pt`, `yolo26n-pose.pt`

## Run locally
```bash
pip install torch torchvision --index-url https://download.pytorch.org/whl/cpu
pip install -r requirements.txt
uvicorn app.main:app --host 0.0.0.0 --port 8000
