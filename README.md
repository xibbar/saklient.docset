# saklient.docset
さくらクラウドのRuby APIをdashで読めるようにするためのリポジトリです。

## 使い方
```
git clone git@github.com:xibbar/saklient.docset.git
```
します。
このディレクトリをdashのdocsetsに登録します。簡単です。

## どうやって作ったか
```
gem install yard
gem install doc_to_dash
```

を実行しておき、

```
yardoc lib/**/*.rb --protected --private --embed-mixins --output-dir doc/yard
```

を実行して、irbの中で

```
DocToDash::DocsetGenerator.new(:doc_input_path => './doc/yard', :docset_name=>"Saklient").run
```

を実行して作りました。
