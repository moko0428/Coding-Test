체육복이 없는 사람이 앞 뒤 번호 사람에게 체육복을 빌려서 체육 수업을 들을 수 있는 사람 수를 알게하는 문제이다.

탐욕법 알고리즘

1. 탐욕 선택 속성
   각 단계에서 ‘최선의 선택’을 했을 때 전체 문제에 대한 최적해를 구할 수 있는 경우를 말합니다. 즉, 각 단계에서 가장 이상적인 선택을 하는 것이 전체적으로 최적의 결과를 가져온다는 것입니다.

2. 최적 부분 구조
   전체 문제의 최적해가 ‘부분 문제의 최적해로 구성’될 수 있는 경우를 말합니다. 즉, 전체 문제를 작은 부분 문제로 나누어 각각의 부분 문제에서 최적의 해를 구한 후 이를 조합하여 전체 문제의 최적해를 구하는 것을 의미합니다.

최대한 이런 느낌으로 구현을 해보고자 했다.

일단 교집합을 제거하기 위해

let actualLost = lost.filter((l) => !reserve.includes(l));
let actualReserve = reserve.filter((r) => !lost.includes(r));

이렇게 체육복을 잃어버렸지만 여분의 체육복이 없는 학생들의 목록과
여분의 체육복이 있지만 체육복을 잃어버리지 않은 학생들의 목록을 만든다.

그렇게 하고 found로 Flag를 만든다음에 비교를 해주는 것이다
