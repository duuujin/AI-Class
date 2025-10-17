# SigLIP
- SigLIP는 softmax 대신 sigmoid 기반 손실함수
- 기존 CLIP에서 사용한 대조학습(COntrastive learning)의 한계는 무엇일까?
    - 어느 정도 이미 멀게 배치한 음성 데이터들에 대해서도 계속 거리를 벌리기 위해 학습이 진행됨
- SigCLIP : CLIP과 달리 일치하지 않는 음성 데이터에 제한된 영향만 받도록 손실함수 디자인을 고침
- CLIP 대비 SigLIP이 압도적인 성능을 보이며 최신 VLM에 널리 활용됨(최근 SigLIP 2도 공개)

# 멀티 모달 정합(Multi-modal Alignment) 응용
- 서로 다른 두 가지 이상의 모달리티(예: 이미지와 텍스트) 간의 공통된 임베이딩 벡터 공간을 구성하는 것
- 서로 다른 모달리티 임베이딩 간 유사도(연관성) 비교 가능
- 대표적인 모델
    - CLIP(OpenAI) : 이미지와 텍스트 간의 Multi-modal Alignment를 효과적으로 수행
    - ImageBind(Meta) : 더 다양한 모달리티(예: 소리, 텍스트, 이미지, 열화상, 깊이맵을 결합)

## VLM의 눈으로 응용
- CLIP 기반 VLM들 리스트
    - BLIP-2 : CLIP + OPT/FlanT5 결합
    - InstructBLIP : BLIP-2의 instruction tuning 버전
    - LLaVA : CLIP + Vicuna
    - MiniGPT-4 : CLIP + Vicuna 기반
    - mPLUG-Owl : CLIP 기반 Alibaba의 VLM
- SigLIP 기반 VLM들 리스트
    - PaLI-X : SigLIP + PaLM 결합
    - SmolVLM
- 최근에는 CLIP, SigLIP의 성공적인 레시피를 기반으로 특화 Vision encoder 모델들이 개발되는 추세
