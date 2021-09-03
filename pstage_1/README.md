# P Stage 1 - Image Classification

  <p align="center">
    <br />
    <a href="memoir.md"><strong>회고록 보러가기 »</strong></a>
    <br />
    <a href="planning_guide.md"><strong>플래닝가이드 보러가기 »</strong></a>
    <br />
  </p>



## 🔥 Final Score

### 🥉Public Leaderboard

- Acc: 81.508
- F1 (macro): 0.766 (11등)

### 🥉Private Leaderboard

- Acc: 80.746
- F1 (macro): 0.754 (13등 - 2위 하락)

---

## 📝 Task Description

COVID-19의 확산으로 우리나라는 물론 전 세계 사람들은 경제적, 생산적인 활동에 많은 제약을 가지게 되었습니다. 우리나라는 COVID-19 확산 방지를 위해 사회적 거리 두기를 단계적으로 시행하는 등의 많은 노력을 하고 있습니다. 과거 높은 사망률을 가진 사스(SARS)나 에볼라(Ebola)와는 달리 COVID-19의 치사율은 오히려 비교적 낮은 편에 속합니다. 그럼에도 불구하고, 이렇게 오랜 기간 동안 우리를 괴롭히고 있는 근본적인 이유는 바로 COVID-19의 강력한 전염력 때문입니다.

감염자의 입, 호흡기로부터 나오는 비말, 침 등으로 인해 다른 사람에게 쉽게 전파가 될 수 있기 때문에 감염 확산 방지를 위해 무엇보다 중요한 것은 모든 사람이 마스크로 코와 입을 가려서 혹시 모를 감염자로부터의 전파 경로를 원천 차단하는 것입니다. 이를 위해 공공 장소에 있는 사람들은 반드시 마스크를 착용해야 할 필요가 있으며, 무엇 보다도 코와 입을 완전히 가릴 수 있도록 올바르게 착용하는 것이 중요합니다. 하지만 넓은 공공장소에서 모든 사람들의 올바른 마스크 착용 상태를 검사하기 위해서는 추가적인 인적자원이 필요할 것입니다.

따라서, 우리는 카메라로 비춰진 사람 얼굴 이미지 만으로 이 사람이 마스크를 쓰고 있는지, 쓰지 않았는지, 정확히 쓴 것이 맞는지 자동으로 가려낼 수 있는 시스템이 필요합니다. 이 시스템이 공공장소 입구에 갖춰져 있다면 적은 인적자원으로도 충분히 검사가 가능할 것입니다.

---

## 😷 Dataset

마스크를 착용하는 건 COIVD-19의 확산을 방지하는데 중요한 역할을 합니다. 제공되는 이 데이터셋은 사람이 마스크를 착용하였는지 판별하는 모델을 학습할 수 있게 해줍니다. 모든 데이터셋은 아시아인 남녀로 구성되어 있고 나이는 20대부터 70대까지 다양하게 분포하고 있습니다. 간략한 통계는 다음과 같습니다.

- 전체 사람 명 수 : 4,500
- 한 사람당 사진의 개수: 7 [마스크 착용 5장, 이상하게 착용(코스크, 턱스크) 1장, 미착용 1장]
- 이미지 크기: (384, 512)

---

## 🔎 Class Description

![](/images/image-20210903122042492.png)

<p align="center">
  아이콘 제작자 <a href="https://www.freepik.com" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/kr/" title="Flaticon">www.flaticon.com</a>
</p>


<br>
<br>

<p align="center">
<div markdown="1">

  | Label |   Mask    | Gender |      Age       |
  | :---: | :-------: | :----: | :------------: |
  |   0   |   Wear    |  Male  |      < 30      |
  |   1   |   Wear    |  Male  | >= 30 and < 60 |
  |   2   |   Wear    |  Male  |     >= 60      |
  |   3   |   Wear    | Female |      < 30      |
  |   4   |   Wear    | Female | >= 30 and < 60 |
  |   5   |   Wear    | Female |     >= 60      |
  |   6   | Incorrect |  Male  |      < 30      |
  |   7   | Incorrect |  Male  | >= 30 and < 60 |
  |   8   | Incorrect |  Male  |     >= 60      |
  |   9   | Incorrect | Female |      < 30      |
  |  10   | Incorrect | Female | >= 30 and < 60 |
  |  11   | Incorrect | Female |     >= 60      |
  |  12   | Not Wear  |  Male  |      < 30      |
  |  13   | Not Wear  |  Male  | >= 30 and < 60 |
  |  14   | Not Wear  |  Male  |     >= 60      |
  |  15   | Not Wear  | Female |      < 30      |
  |  16   | Not Wear  | Female | >= 30 and < 60 |
  |  17   | Not Wear  | Female |     >= 60      |

</div>
</p>