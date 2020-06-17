# 3sem_FinalProject
Финальный конкурс 3 семестра ТехноСферы (https://www.kaggle.com/c/ranking-long-tail-queries-ts-spring-2020/leaderboard), score: 0.77181/0.78195

1. Подсчет статистик:
Собрать файлы из getting_features_JAVA(для удобства закинул jar-ник), запустить на хадупе следующие команды:
- hadoop jar User_relev-1.0-SNAPSHOT.jar ClickJob *папка со статистиками* ir_2_result_q
- hadoop jar User_relev-1.0-SNAPSHOT.jar FullJob *папка со статистиками* ir_2_result_u
- hadoop jar User_relev-1.0-SNAPSHOT.jar HostJob *папка со статистиками* ir_2_result_h
- hadoop jar User_relev-1.0-SNAPSHOT.jar HostqJob *папка со статистиками* ir_2_result_hq
- hadoop jar User_relev-1.0-SNAPSHOT.jar UrlQJob *папка со статистиками* ir_2_result_uq
- hadoop jar User_relev-1.0-SNAPSHOT.jar sDBNJob *папка со статистиками* ir_2_result_sDBN

2. предобработка+Семантические/текстовые фичи:
В папке preprocess_and_getting_features_PY cоздать папку "Data", в нее добавить "docs.tsv", "sample.csv", "train.marks.tsv", "url.data", "queries_b.txt"(есть в репозитории), "cc.ru.300.bin.gz" (https://fasttext.cc/docs/en/crawl-vectors.html  модель "Russian"). Запустить Normolizer.ipynb, запустить все остальные ноутбуки для подсчета фичей (USEFeatures.ipynb и FastTextFeatures.ipynb желательно запускать на колабе)

3. Добавить все полученные фичи(ir_2_result* в папку new_feat, fasttextfeat.txt и USE_feat* в папку feat_title) в папку main, запустить Project_V2.ipynb (желательно запускать на колабе)
