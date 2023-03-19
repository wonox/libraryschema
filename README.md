# 大学図書館の概念スキーマ

大学図書館を一つのデータベースと見立て、概念スキーマをER図風に書いてみた。


```mermaid
flowchart TB

accessible(アクセス可能化)
kb(所在データ/ナレッジベース)
licence(ライセンスデータ)
contents(コンテンツ)
fullfilment(受入/購入/契約)
metadata(メタデータ/書誌)
logistics(物流制御)
archive(アーカイブ/ストレージ/書架/書庫)
authenticate(認証/認可)
analyze(アクセス/利用分析)

研究者 --> contents
contents --> accessible
accessible --> metadata
accessible --> kb
accessible --> fullfilment
accessible --> metadata
kb --> contents
kb --> logistics
kb --> access

subgraph contents
    画像/動画/音声
    図書/雑誌
    論文
    研究データ
end

subgraph publish
    access
end
subgraph kb
   subgraph holdings
     所蔵ID
     DOI
   end
   licence
end
subgraph arcive
end
subgraph ユーザー管理
end
subgraph 検索用インデクス
end 
subgraph fullfilment
end 
subgraph test
end
subgraph logistics
end 
subgraph authenticate
   利用/アクセス可
end
subgraph access
end 
subgraph test
end  
one --> two

```

## 考察

- publishをコンテンツのアクセス可能化とそれに紐づくメタデータ管理、ライセンス管理、アクセス制御と捉えると、昔ながらの図書もEJもリポジトリや研究データもデジタルアーカイブも共通に考えられる。
- 所蔵に紐づくライセンスデータと、それを認証・認可に紐づけると、貸出とかアクセス管理になる



