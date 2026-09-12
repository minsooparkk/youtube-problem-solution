# 설계 근거

공식 자료 확인일: 2026-09-12.

6단계 서사, 첫 60초 기준, 10분 시간 배분은 사용자의 기획 방식을 구현한 편집 기준이다. OpenAI 공식 영상 제작 프레임워크나 ‘ASTRA’ 약어 기법이 아니다.

- [GPT-6 Astra prompting best practices](https://developers.openai.com/api/docs/guides/latest-model?model=gpt-6-astra#prompting-best-practices): 핵심을 일찍 제시하는 문체, 구체적인 스타일, 자율 진행과 완성 기준을 반영했다.
- [Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra): 불필요한 지시를 줄이고 적용 범위와 완료 지점을 명확히 했다. 내부 사고 절차는 강제하지 않는다.
- [OpenAI Prompt engineering](https://developers.openai.com/api/docs/guides/prompt-engineering): 역할·지시·문맥을 구분하고 예시는 필요할 때만 참고하게 했다.
- [Codex Build skills](https://learn.chatgpt.com/docs/build-skills): SKILL.md의 이름·설명과 본문을 사용한다. 개인 설치 위치는 ~/.agents/skills이며 명시적 호출은 $youtube-problem-solution이다.
- [Claude Code skills](https://code.claude.com/docs/en/skills): 같은 SKILL.md를 ~/.claude/skills에 배치해 /youtube-problem-solution으로 호출한다.

SKILL.md에는 공통 name·description만 사용한다. 특정 모델, API 키, 전용 도구 이름, 운영체제별 명령, 다른 스킬 의존성을 요구하지 않는다. 보조 자료는 상대 경로로 연결해 폴더를 이동해도 사용할 수 있다.
