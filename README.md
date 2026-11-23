# leadus-info/.github

leadus-info organizationの全リポジトリに共通する、GitHubの既定ファイル(コミュニティヘルスファイル)と組織プロフィールを管理するリポジトリです。

## 運用ルール

- **`main`ブランチへの直接変更は禁止**。反映は`main`以外の作業用ブランチからのPull Requestによるマージのみで行う。
- このリポジトリの変更は、organizationの全リポジトリのissue・PRの作成画面に即座に反映される。issueテンプレートを変更する場合は、YAMLとして読み込めることを確認してからPRを出す(読み込めないテンプレートは、エラーにならず表示されなくなるだけで気づきにくい)。
- このリポジトリには、GitHubの既定ファイルとして置く必要があるものだけを置く。文書の本体は[docs](https://github.com/leadus-info/docs)で管理する(下記「管理するもの」参照)。

## 管理するもの

| ファイル | 内容 |
| --- | --- |
| [CONTRIBUTING.md](CONTRIBUTING.md) | 既定の貢献ガイド。[docs](https://github.com/leadus-info/docs)の貢献ガイド・執筆ガイドへの案内のみを書く |
| [.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/) | 既定のissueテンプレート(新規記事の提案・既存記事の問題報告)と`config.yml` |
| [.github/pull_request_template.md](.github/pull_request_template.md) | 既定のPRテンプレート |
| [profile/README.md](profile/README.md) | organizationのページに表示されるプロフィール |

貢献の方法・執筆ルールなどの文書の本体はdocsで管理します。このリポジトリには、GitHubの既定ファイルとして置く必要があるものだけを置きます。

## 既定ファイルが適用される条件

- このリポジトリがpublicであれば、organization内の全リポジトリ(privateを含む)に適用されます。
- 適用されるのは、そのリポジトリに同じ種類のファイルがない場合のみです。
  - CONTRIBUTING.md・PRテンプレートは、ファイルの種類ごとに判定されます。
  - issueテンプレートは`.github/ISSUE_TEMPLATE/`フォルダ単位で判定されます。リポジトリに自前の`.github/ISSUE_TEMPLATE/`がある場合(`config.yml`のみでも)、既定のissueテンプレートは1つも使われません。
- LICENSEは既定にできないため、各リポジトリに置きます。

## リポジトリごとの扱い

| リポジトリ | issueテンプレート | CONTRIBUTING.md・PRテンプレート |
| --- | --- | --- |
| 科目リポジトリ(`math`・`phys`等) | 既定を使う(自前のものを置かない) | 既定を使う(自前のものを置かない) |
| 科目以外(`docs`・`platform`・`assets-web`・`agent`) | 自前の`.github/ISSUE_TEMPLATE/config.yml`で既定を打ち消す | 既定を使う |

issueテンプレートは科目リポジトリ向け(新規記事の提案・既存記事の問題報告)のため、科目以外のリポジトリでは打ち消しています。

## 参考

- [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [Customizing your organization's profile](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile)
