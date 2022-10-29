# statistical_experiments_with_samples
Проведение статистических экспериментов при работе с выборками.
# Основная идея
При прочность бетона обладает ярко выраженной вариативностью (которая в нормативной и научной литературе описана как нормальное распределение).
Задача преобразуется в работу с "генеральными совокупностями" различного вида бетонов "Data А" (В20 по [СП63](https://docs.cntd.ru/document/554403082) ) и "Data B" (В25 по [СП63](https://docs.cntd.ru/document/554403082)).

```python
  df = pd.DataFrame()
  mu_A, mu_B = 15, 18.5
  sigma_A, sigma_B = 0.1732* mu_A , 0.135* mu_B
  np.random.seed(42)
  data_A = np.random.normal(1.66,1,10_000)*sigma_A + mu_A
  data_B = np.random.normal(1.66,1,10_000)*sigma_B + mu_B

  df['data_A'] = data_A
  df['data_B'] = data_B

  plt.hist(df['data_A'], bins=50, alpha=0.5, label='data_A')
  plt.hist(df['data_B'], bins=50, alpha=0.5, label='data_B')
  plt.legend(loc='upper right')
  plt.show()
```
<body>
  <p><img src="https://user-images.githubusercontent.com/111303182/198828826-7fc965bc-40bd-4806-893c-ec4e0f7e2ed1.png"></p>
</body>
# Публикация статьи
Кузнецов В.В. ПРОВЕДЕНИЕ ЧИСЛЕННОГО ЭКСПЕРИМЕНТА С ОЦЕНКОЙ КОЭФФИЦИЕНТА ВАРИАЦИИ ПРОЧНОСТИ БЕТОНА ПО ВЫБОРКЕ // Вопросы технических и физико-математических наук в свете современных исследований: сб. ст. по матер. LV-LVI междунар. науч.-практ. конф. № 9-10(47). – Новосибирск: СибАК, 2022.
