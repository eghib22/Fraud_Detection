# Fraud_Detection
მოკლედ პროექტის მიზანია ისეთი მოდელის დატრენინგება რონელიც ამიცნობს ტრანზაქციებიდან რომლებია თაღლითობა.
მე დავატრენინგე ოთხი მოდელი: logistic regression, random foresti, xgboost, adaboost
თითოეული მოდელის დატრენინგება შესაბამის model_experiment_{modelis saxeli} ფაილშია
გადავიყვანე კატეგორიული ცვლადები რიცხვითში ordinal encoder-ით, missing ველიუები უბრალოდ -999-ით ჩავანაცვლე.
მიმაჩნია რომ ეს data preprocessing, რაც ყველა მოდელს კარგად ერგება და ფაიფლაინს აქვს გაწერილი, სავსებით საკმარისია.
თრეინ დატასეტი გავსპლიტე 80/20 შფარდებით და თითოეული მოდელი დავატრენინგე
საუკეთესო შედეგი ქონდა xgboostს, თუმცა ტესტზე რომ გავუშვი ინფერენს ფაილში დიდი სხვაობა იყო auc ქულებს შორის რის გამოც ვფიქრობ რომ მოხდა overfitting
ამის გამოსასწორებლად early stopping და რეგულარიზაცია ვცადე, ასევე, შევამცირე learning rate.

 https://dagshub.com/eghib22/Fraud_Detection.mlflow/#/experiments/0?searchFilter=&orderByKey=attributes.start_time&orderByAsc=false&startTime=ALL&lifecycleFilter=Active&modelVersionFilter=All+Runs&datasetsFilter=W10%3D
