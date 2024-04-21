# 跨雲容錯負載平衡及網頁自動化部署管理

## 項目概述
這個項目設計了一個在AWS和Azure雲平台上部署高可用的Wordpress服務的解決方案，並利用了Terraform和Ansible進行自動化部署和管理。

## 主要特點
- **多雲容錯**: 利用AWS和Azure的強大能力，實現高可用性。
- **自動化部署**: 利用Terraform和Ansible實現基礎設施和軟體的自動部署。
- **簡化管理**: 通過自動化大幅減少手動配置和維護工作，提高運維效率。

## 技術棧
- AWS & Azure 雲平台
- Terraform
- Ansible
- CI/CD Pipelines

## 安裝

1.首先確保您的電腦上已經安裝了requirements.txt 相關開發內容
2.你需要在AWS 私有雲和Azure雲上都有賬戶, 在相對應的目錄下必須複製你的進接資訊。
3.在AWS的IAM使用者權限設定，進行AWS存取設定，並把進接金鑰（Access key）及密鑰（Secret access key）妥善保存。同理，對於Azure，需要設定租戶識別碼（Tenant ID）、訂用識別碼（Subscription ID）、客戶應用識別碼（ Client ID），和密鑰（Secret Key）。請在設定文件中設定這些參數。
4.您可以使用Terraform來設定基礎設施。根據你的需求修改main.tf文件，然後在終端機裡依次輸入以下命令：
terraform init
terraform apply
5.透過Ansible來進行應用程序的自動部署配置. 運行以下命令:
 ansible-playbook main.yml

6.現在，你已經成功地在AWS和Azure雲平台上部署了垂直可擴展的wordpress網頁服務。