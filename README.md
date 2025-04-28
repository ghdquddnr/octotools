<a name="readme-top"></a>

<div align="center">
<img src="https://raw.githubusercontent.com/octotools/octotools/refs/heads/main/assets/octotools.svg" alt="OctoTools Logo" width="100">
</div>

# OctoTools: 복잡한 추론을 위한 확장 가능한 도구를 갖춘 에이전트 프레임워크


<!--- BADGES: START --->
[![GitHub 라이선스](https://img.shields.io/badge/License-MIT-green.svg?logo=github)](https://lbesson.mit-license.org/)
[![Arxiv](https://img.shields.io/badge/arXiv-2502.11271-B31B1B.svg?logo=arxiv)](https://arxiv.org/abs/2502.11271)
[![Huggingface 데모](https://img.shields.io/badge/Huggingface-Demo-FFD21E.svg?logo=huggingface)](https://huggingface.co/spaces/OctoTools/octotools)
[![PyPI](https://img.shields.io/badge/octotoolkit-0.2.0-2176BC?logo=python)](https://pypi.org/project/octotoolkit/)
[![YouTube](https://img.shields.io/badge/YouTube-튜토리얼-FF0000?logo=youtube)](https://www.youtube.com/watch?v=4828sGfx7dk)
[![웹사이트](https://img.shields.io/badge/Website-OctoTools-D41544?logo=octopusdeploy)](https://octotools.github.io/)
[![도구 카드](https://img.shields.io/badge/Tool_Cards-OctoTools-2176BC?logo=octopusdeploy)](https://octotools.github.io/#tool-cards)
[![시각화](https://img.shields.io/badge/Visualization-OctoTools-D41544?logo=octopusdeploy)](https://octotools.github.io/#visualization)
[![커버리지](https://img.shields.io/badge/Coverage-OctoTools-2176BC.svg?logo=x)](https://x.com/lupantech/status/1892260474320015861)
[![Slack](https://img.shields.io/badge/Slack-OctoTools-D41544.svg?logo=slack)](https://join.slack.com/t/octotools/shared_invite/zt-3485ikfas-zMTbFbuodJmET~R6KXHEGw)
<!-- [![Discord](https://img.shields.io/badge/Discord-OctoTools-D41544?logo=discord)](https://discord.gg/kgUXdZHgNG) -->
<!--- BADGES: END --->


## 업데이트


### 뉴스

- **2025-04-19** 📦: PyPI에서 Python 패키지를 출시했습니다! [pypi.org/project/octotoolkit](https://pypi.org/project/octotoolkit)에서 확인하실 수 있습니다. 자세한 설치 방법은 [설치 가이드](https://github.com/octotools/octotools?tab=readme-ov-file#installation)를 참고해 주세요.
- **2025-04-17** 🚀: 더 다양한 LLM 엔진을 지원합니다! 지원되는 LLM 엔진 목록은 [여기](https://github.com/octotools/octotools?tab=readme-ov-file#supported-llm-engines)에서 확인하실 수 있습니다.
- **2025-03-08** 📺: [Discover AI](https://www.youtube.com/@code4AI)의 YouTube 튜토리얼에 OctoTools가 소개되었습니다! [여기](https://www.youtube.com/watch?v=4828sGfx7dk)에서 영상을 시청하실 수 있습니다.
- **2025-02-16** 📄: 논문이 ArXiv에 프리프린트로 게시되었습니다! [여기](https://arxiv.org/abs/2502.11271)에서 확인하실 수 있습니다.


### TODO

Stay tuned, we're working on the following:

- [X] Add support for Anthropic LLM
- [X] Add support for Together AI LLM
- [X] Add support for DeepSeek LLM
- [X] Add support for Gemini LLM
- [X] Add support for Grok LLM
- [X] Release Python package on PyPI
- [ ] Add support for vLLM LLM (to support custom models, in progress)
- [ ] Add support for litellm LLM (to support API models)

**TBD**: We're excited to collaborate with the community to expand OctoTools to more tools, domains, and beyond! Join our [Slack](https://join.slack.com/t/octotools/shared_invite/zt-3485ikfas-zMTbFbuodJmET~R6KXHEGw) or reach out to [Pan Lu](https://lupantech.github.io/) to get started!

## 시작하기

### YouTube 튜토리얼

[Discover AI](https://www.youtube.com/@code4AI)의 YouTube 채널에서 OctoTools 튜토리얼 영상을 확인하실 수 있습니다!

<div align="center">
  <a href="https://www.youtube.com/watch?v=4828sGfx7dk">
    <img src="https://img.youtube.com/vi/4828sGfx7dk/maxresdefault.jpg" alt="OctoTools 튜토리얼" width="100%">
  </a>
</div>

### 소개

**OctoTools**는 다양한 도메인에서 복잡한 추론을 수행하기 위한 학습이 필요 없는, 사용자 친화적이며 쉽게 확장 가능한 오픈소스 에이전트 프레임워크입니다. **OctoTools**는 도구 기능을 캡슐화하는 표준화된 **도구 카드**, 고수준 및 저수준 계획을 위한 **플래너**, 그리고 도구 사용을 실행하는 **실행기**를 도입했습니다.

**도구 카드**는 도구 사용 메타데이터를 정의하고 다양한 도구를 캡슐화하여, 추가 학습이나 프레임워크 개선 없이도 새로운 도구를 학습 없이 통합할 수 있게 합니다. (2) **플래너**는 전역 목표를 해결하고 단계별로 작업을 세분화하기 위해 고수준 및 저수준 계획을 관리합니다. (3) **실행기**는 실행 가능한 명령을 생성하고 컨텍스트에 구조화된 결과를 저장하여 도구 호출을 인스턴스화합니다. 최종 답변은 컨텍스트의 전체 궤적에서 요약됩니다. 또한, *작업별 도구셋 최적화 알고리즘*은 다운스트림 작업에 유용한 도구의 하위 집합을 학습합니다.

![framework_overall](https://raw.githubusercontent.com/octotools/octotools/refs/heads/main/assets/models/framework_overall.png)
![framework_example](https://raw.githubusercontent.com/octotools/octotools/refs/heads/main/assets/models/framework_example.png)

**OctoTools**는 16개의 다양한 작업(MathVista, MMLU-Pro, MedQA, GAIA-Text 등)에서 일반성을 검증했으며, GPT-4o 대비 평균 9.3%의 정확도 향상을 달성했습니다. 또한, 동일한 도구 세트가 주어졌을 때 AutoGen, GPT-Functions, LangChain보다 최대 10.6% 더 나은 성능을 보여줍니다.

<p align="center">  
    <img src="https://raw.githubusercontent.com/octotools/octotools/refs/heads/main/assets/result/main_scores_bar_chart.png" width="50%">
</p>


### 지원되는 LLM 엔진

GPT-4o, Claude 3.5 Sonnet, Gemini 1.5 Pro 등 다양한 LLM 엔진을 지원합니다.

| 모델 패밀리 | 엔진 (멀티모달) | 엔진 (텍스트 전용) | 공식 모델 목록 |
|--------------|-------------------|--------------------| -------------------- |
| OpenAI | `gpt-4-turbo`, `gpt-4o`, `gpt-4o-mini`,  `gpt-4.1`,  `gpt-4.1-mini`, `gpt-4.1-nano`, `o1`, `o3`, `o1-pro`, `o4-mini` | `gpt-3.5-turbo`, `gpt-4`, `o1-mini`, `o3-mini` | [OpenAI 모델](https://platform.openai.com/docs/models) |
| Anthropic | `claude-3-haiku-20240307`, `claude-3-sonnet-20240229`, `claude-3-opus-20240229`, `claude-3-5-sonnet-20240620`, `claude-3-5-sonnet-20241022`, `claude-3-5-haiku-20241022`, `claude-3-7-sonnet-20250219` | | [Anthropic 모델](https://docs.anthropic.com/en/docs/about-claude/models/all-models) |
| TogetherAI | 대부분의 멀티모달 모델, `meta-llama/Llama-4-Scout-17B-16E-Instruct`, `Qwen/QwQ-32B`, `Qwen/Qwen2-VL-72B-Instruct` 포함 | 대부분의 텍스트 전용 모델, `meta-llama/Llama-3-70b-chat-hf`, `Qwen/Qwen2-72B-Instruct` 포함 | [TogetherAI 모델](https://api.together.ai/models) |
| DeepSeek |  | `deepseek-chat`, `deepseek-reasoner` | [DeepSeek 모델](https://api-docs.deepseek.com/quick_start/pricing) |
| Gemini | `gemini-1.5-pro`, `gemini-1.5-flash-8b`, `gemini-1.5-flash`, `gemini-2.0-flash-lite`, `gemini-2.0-flash`, `gemini-2.5-pro-preview-03-25` |  |  [Gemini 모델](https://ai.google.dev/gemini-api/docs/models) |
| Grok | `grok-2-vision-1212`, `grok-2-vision`, `grok-2-vision-latest` | `grok-3-mini-fast-beta`, `grok-3-mini-fast`, `grok-3-mini-fast-latest`, `grok-3-mini-beta`, `grok-3-mini`, `grok-3-mini-latest`, `grok-3-fast-beta`, `grok-3-fast`, `grok-3-fast-latest`, `grok-3-beta`, `grok-3`, `grok-3-latest` | [Grok 모델](https://docs.x.ai/docs/models#models-and-pricing) |

> 참고: TogetherAI 모델을 사용하실 경우, 모델 문자열에 'together-' 접두사를 붙여주세요. 예: `together-meta-llama/Llama-4-Scout-17B-16E-Instruct`. 다른 커스텀 엔진을 사용하시려면 [factory.py](https://github.com/OctoTools/OctoTools/blob/main/octotools/engine/factory.py) 파일을 수정하고 해당 인터페이스 파일을 추가하시면 됩니다. 풀 리퀘스트는 환영합니다!

## 설치 방법

현재 OctoTools를 설치하는 방법은 두 가지가 있습니다. 대부분의 경우 [표준 설치](https://github.com/octotools/octotools?tab=readme-ov-file#1-standard-installation)로 충분합니다. 하지만 [벤치마크](https://github.com/octotools/octotools/tree/main/tasks)를 복제하고 코드를 직접 수정하시려면 Github에서 여러 bash 스크립트가 필요합니다. 이 경우 [편집 가능한 설치](https://github.com/octotools/octotools?tab=readme-ov-file#2-editable-installation)를 권장합니다.

### 1. 표준 설치

conda 환경을 생성하고 의존성을 설치합니다:

```sh
conda create -n octotools python=3.10
conda activate octotools
pip install octotoolkit
```

`.env` 파일을 만들고 `OPENAI_API_KEY`, `GOOGLE_API_KEY`, `GOOGLE_CX` 등을 설정합니다. 예시:

```sh
# .env 파일의 내용

# LLM 기반 모듈 및 도구에 사용
OPENAI_API_KEY=<your-api-key-here> # OpenAI LLM을 사용하려는 경우
ANTHROPIC_API_KEY=<your-api-key-here> # Anthropic LLM을 사용하려는 경우
TOGETHER_API_KEY=<your-api-key-here> # TogetherAI LLM을 사용하려는 경우
DEEPSEEK_API_KEY=<your-api-key-here> # DeepSeek LLM을 사용하려는 경우
GOOGLE_API_KEY=<your-api-key-here> # Gemini LLM을 사용하려는 경우
XAI_API_KEY=<your-api-key-here> # Grok LLM을 사용하려는 경우

# Google 검색 도구에 사용
GOOGLE_API_KEY=<your-api-key-here>
GOOGLE_CX=<your-cx-here>

# 고급 객체 감지 도구에 사용 (선택사항)
DINO_KEY=<your-dino-key-here>
```

[Google Custom Search API](https://developers.google.com/custom-search/v1/overview) 문서에 따라 Google API 키와 Google CX를 획득하세요.

### 2. 편집 가능한 설치

새로운 환경에서 시작합니다:
```sh
conda create -n octotools python=3.10
conda activate octotools
```

[github 저장소](https://github.com/octotools/octotools)를 클론합니다:
```sh
git clone https://github.com/octotools/octotools.git
```

루트 디렉토리(`pyproject.toml`이 있는 디렉토리)에서 다음 명령을 실행합니다:
```sh
pip install -e .
```

(선택사항) 벤치마크 실험을 병렬로 실행하기 위해 `parallel`을 설치합니다:

```sh
sudo apt-get update
sudo apt-get install parallel
```

## 빠른 시작

새로운 폴더에서 API 키를 설정하기 위해 다음 코드를 붙여넣으세요:
```py
# API 키를 .env 파일에 넣어주세요
import dotenv
dotenv.load_dotenv()

# 또는 API 키를 직접 설정할 수 있습니다
import os
os.environ["OPENAI_API_KEY"] = "your_api_key"
```

그런 다음 기본 솔버를 테스트하기 위해 다음 코드를 붙여넣으세요:
```py
# 솔버 가져오기
from octotools.solver import construct_solver

# LLM 엔진 이름 설정
llm_engine_name = "gpt-4o"

# 솔버 생성
solver = construct_solver(llm_engine_name=llm_engine_name)

# 사용자 쿼리 해결
output = solver.solve("프랑스의 수도는 무엇인가요?")
print(output["direct_output"])

# 마찬가지로 사진을 전달할 수도 있습니다
output = solver.solve("이 물건의 프랑스어 이름은 무엇인가요?", image_path="<PATH_TO_IMG>")
print(output["direct_output"])
```

결과와 함께 모든 중간 내용을 확인하실 수 있습니다.

더 자세한 jupyter notebook 예제는 [examples/notebooks](https://github.com/octotools/octotools/tree/main/examples/notebooks) 폴더에서 확인하실 수 있습니다.

## 도구 상자에서 도구 테스트하기 (Github의 테스트 스크립트 필요)

`Python_Code_Generator_Tool`을 예시로, 다음을 실행하여 도구의 가용성을 테스트할 수 있습니다:

```sh
cd src/octotools/tools/python_code_generator
python tool.py
```

예상 출력:

```
실행 결과: {'printed_output': '리스트의 모든 숫자의 합은: 15', 'variables': {'numbers': [1, 2, 3, 4, 5], 'total_sum': 15}}
```

도구 상자에서 사용 가능한 모든 도구를 테스트하려면 다음을 실행하세요:

```sh
cd src/octotools/tools
source test_all_tools.sh
```

예상 테스트 로그:

```
advanced_object_detector 테스트 중...
✅ advanced_object_detector 통과

arxiv_paper_searcher 테스트 중...
✅ arxiv_paper_searcher 통과

...

wikipedia_knowledge_searcher 테스트 중...
✅ wikipedia_knowledge_searcher 통과

모든 도구 테스트 완료
실패: 0
```

## 벤치마크에서 추론 실행하기 (Github의 Bash 스크립트 필요)

[CLEVR-Math](https://huggingface.co/datasets/dali-does/clevr-math)를 예시로, 벤치마크에서 추론을 실행하려면:

```sh
cd src/octotools/tasks

# GPT-4만 사용하여 clevr-math에서 추론 실행
source clevr-math/run_gpt4o.sh
```

More benchmarks are available in the [tasks](https://octotools.github.io/#tasks).


## 실험


### 주요 결과

**OctoTools** 프레임워크의 일반성을 입증하기 위해, 두 가지 모달리티, 다섯 가지 도메인, 네 가지 추론 유형에 걸친 16개의 다양한 벤치마크에 대한 종합적인 평가를 수행했습니다. 이러한 벤치마크는 시각적 이해, 수치 계산, 지식 검색, 다단계 추론 등 다양한 복잡한 추론 작업을 포함합니다.


<p align="center">
    <img src="https://raw.githubusercontent.com/octotools/octotools/refs/heads/main/assets/result/result_table_1.png" width="100%">
</p>


더 많은 결과는 [논문](https://arxiv.org/pdf/2502.11271)이나 [프로젝트 페이지](https://octotools.github.io/)에서 확인하실 수 있습니다.


### 심층 분석

프레임워크를 이해하는 데 도움이 되는 심층 분석을 제공합니다. 예를 들어, 16개 작업에서 **OctoTools**와 그 기준 모델들의 도구 사용을 시각화했습니다. **OctoTools**는 작업별 도전 과제를 해결하기 위해 다양한 외부 도구를 활용하는 것으로 나타났습니다. 더 많은 발견은 [논문](https://arxiv.org/pdf/2502.11271)이나 [프로젝트 페이지](https://octotools.github.io/#analysis)에서 확인하실 수 있습니다.

<a align="center">
    <img src="https://raw.githubusercontent.com/octotools/octotools/refs/heads/main/assets/result/tool_usage_ours_baselines.png" width="100%">
</a>

### 예시 시각화

프레임워크를 이해하는 데 도움이 되는 예시 시각화를 제공합니다. [프로젝트 페이지](https://octotools.github.io/#visualization)에서 확인하실 수 있습니다.

<p align="center">  
    <a href="https://octotools.github.io/#visualization">
        <img src="https://raw.githubusercontent.com/octotools/octotools/refs/heads/main/assets/result/example_visualization.png" width="80%">
    </a>
</p>


## OctoTools 커스터마이징

각 도구 카드의 설계는 **OctoTools** 프레임워크에 대해 모듈화되어 있어, 사용자가 기본 프레임워크나 에이전트 로직을 수정하지 않고도 다양한 도구를 통합할 수 있습니다. 새로운 도구 카드를 최소한의 노력으로 추가, 교체 또는 업데이트할 수 있어, 작업의 복잡성이 증가함에 따라 **OctoTools**를 견고하고 확장 가능하게 만듭니다.

<p align="center">
    <a href="https://octotools.github.io/#tool_cards">
        <img src="https://raw.githubusercontent.com/octotools/octotools/refs/heads/main/assets/models/tool_cards.png" width="100%">
    </a>
</p>

자신의 작업에 맞게 **OctoTools**를 커스터마이징하려면:

1. **새로운 도구 카드 추가**: [기존 도구](https://github.com/OctoTools/OctoTools/tree/main/octotools/tools)의 구조를 따라 도구를 구현하세요.

2. **기존 도구 교체 또는 업데이트**: 도구 상자에서 도구를 교체하거나 업데이트할 수 있습니다. 예를 들어, 오픈소스 모델을 사용하여 이미지에서 객체를 감지하는 [`Object_Detector_Tool`](https://github.com/OctoTools/OctoTools/blob/main/octotools/tools/object_detector/tool.py)을 제공합니다. 또한 API 호출을 사용하여 이미지에서 객체를 감지하는 [`Advanced_Object_Detector_Tool`](https://github.com/OctoTools/OctoTools/blob/main/octotools/tools/advanced_object_detector/tool.py)이라는 대체 도구도 제공합니다.

3. **작업에 도구 활성화**: [tasks/solve.py](https://github.com/OctoTools/OctoTools/blob/main/octotools/tasks/solve.py)에서 `enabled_tools` 인수를 설정하여 전체 도구 세트 또는 도구의 하위 집합을 자신의 작업에 활성화할 수 있습니다.


## 리소스

### 영감

이 프로젝트는 여러 주목할 만한 프로젝트에서 영감을 받았습니다:

- 📕 [Chameleon](https://github.com/lupantech/chameleon-llm) – Chameleon은 LLM에 도구를 추가하는 초기 시도로, 주요 영감의 원천입니다. 천 리 길도 한 걸음부터 시작합니다.
- 📘 [TextGrad](https://github.com/mert-y/textgrad) – TextGrad의 혁신적이고 우아한 프레임워크 설계에 감탄하고 감사합니다.
- 📗 [AutoGen](https://github.com/microsoft/autogen) – 에이전트 시스템 구축에 뛰어난 트렌디한 프로젝트입니다.
- 📙 [LangChain](https://github.com/langchain-ai/langchain) – 풍부한 기능으로 유명한 에이전트 시스템 구축을 위한 강력한 프레임워크입니다.


### 인용
```bibtex
@article{lu2025octotools,
    title={OctoTools: An Agentic Framework with Extensible Tools for Complex Reasoning},
    author={Lu, Pan and Chen, Bowen and Liu, Sheng and Thapa, Rahul and Boen, Joseph and Zou, James},
    journal = {arXiv preprint arXiv:2502.11271},
    year={2025}
}
```

### 우리 팀
<table>
	<tbody>
		<tr>
            <td align="center">
                <a href="https://lupantech.github.io/">
                    <img src="https://avatars.githubusercontent.com/u/17663606?v=4" width="100;" alt="lupantech"/>
                    <br />
                    <sub><b>Pan Lu</b></sub>
                </a>
            </td>
            <td align="center">
                <a href="https://bowen118.github.io/">
                    <img src="https://bowen118.github.io/assets/img/prof_pic.jpg" width="100;" alt="bowen118"/>
                    <br />
                    <sub><b>Bowen Chen</b></sub>
                </a>
            </td>
            <td align="center">
                <a href="https://shengliu66.github.io/">
                    <img src="https://shengliu66.github.io/profile.jpg" width="100;" alt="shengliu66"/>
                    <br />
                    <sub><b>Sheng Liu</b></sub>
                </a>
            </td>
            <td align="center">
                <a href="https://rthapa84.github.io/">                    <img src="https://rthapa84.github.io/assets/img/prof_pic.jpg?2e8380ce955beb4381c1f3918859cf5e" height="100" width="100" alt="rthapa84"/>
                    <br />
                    <sub><b>Rahul Thapa</b></sub>
                </a>
            </td>
            <td align="center">
                <a href="https://dbds.stanford.edu/people/joseph-boen/">
                    <img src="https://dbds.stanford.edu/wp-content/uploads/2023/08/joseph-boen.jpg)" width="100;" alt="josephboen"/>
                    <br />
                    <sub><b>Joseph Boen</b></sub>
                </a>
            </td>
            <td align="center">
                <a href="https://www.james-zou.com/">
                    <img src="https://static.wixstatic.com/media/0f3e8f_cfa7e327b97745ddb8c4a66454b5eb3e~mv2.jpg/v1/fill/w_318,h_446,al_c,q_80,usm_0.66_1.00_0.01,enc_avif,quality_auto/46824428A5822_ForWeb.jpg" height="100;" alt="jameszou"/>
                    <br />
                    <sub><b>James Zou</b></sub>
                </a>
            </td>
		</tr>
	<tbody>
</table>


### 기여자

OctoTools에 대한 오픈소스 기여를 정말 기대하고 있습니다! 기여, 협업 또는 이슈 보고에 관심이 있으시다면 주저하지 말고 연락해 주세요!

여러분의 피드백과 제안도 기대하고 있습니다!

### 스타 히스토리

[![Star History Chart](https://api.star-history.com/svg?repos=octotools/octotools&type=Date)](https://www.star-history.com/#octotools/octotools&Date)

<p align="right" style="font-size: 14px; color: #2176bc; margin-top: 20px;">
  <a href="#readme-top" style="text-decoration: none; color: blue; font-weight: bold;">
    ↑ 맨 위로 ↑
  </a>
</p>
