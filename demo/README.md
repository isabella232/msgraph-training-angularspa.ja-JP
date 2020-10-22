# <a name="how-to-run-the-completed-project"></a><span data-ttu-id="02621-101">完了したプロジェクトを実行する方法</span><span class="sxs-lookup"><span data-stu-id="02621-101">How to run the completed project</span></span>

## <a name="prerequisites"></a><span data-ttu-id="02621-102">前提条件</span><span class="sxs-lookup"><span data-stu-id="02621-102">Prerequisites</span></span>

<span data-ttu-id="02621-103">このフォルダーで完了したプロジェクトを実行するには、次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="02621-103">To run the completed project in this folder, you need the following:</span></span>

- <span data-ttu-id="02621-104">開発用のコンピューターにインストールされている[node.js](https://nodejs.org) 。</span><span class="sxs-lookup"><span data-stu-id="02621-104">[Node.js](https://nodejs.org) installed on your development machine.</span></span> <span data-ttu-id="02621-105">Node.js を持っていない場合は、「ダウンロードオプション」の前のリンクにアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="02621-105">If you do not have Node.js, visit the previous link for download options.</span></span> <span data-ttu-id="02621-106">(**注:** このチュートリアルは、ノードバージョン12.16.1 を使用して作成されています。</span><span class="sxs-lookup"><span data-stu-id="02621-106">(**Note:** This tutorial was written with Node version 12.16.1.</span></span> <span data-ttu-id="02621-107">このガイドの手順は、他のバージョンでは動作しますが、テストされていません。)</span><span class="sxs-lookup"><span data-stu-id="02621-107">The steps in this guide may work with other versions, but that has not been tested.)</span></span>
- <span data-ttu-id="02621-108">開発用コンピューターにインストールされている[角度 CLI](https://cli.angular.io/) 。</span><span class="sxs-lookup"><span data-stu-id="02621-108">[Angular CLI](https://cli.angular.io/) installed on your development machine.</span></span>
- <span data-ttu-id="02621-109">Outlook.com 上のメールボックスを持つ個人の Microsoft アカウント、または Microsoft 職場または学校のアカウントのいずれか。</span><span class="sxs-lookup"><span data-stu-id="02621-109">Either a personal Microsoft account with a mailbox on Outlook.com, or a Microsoft work or school account.</span></span>

<span data-ttu-id="02621-110">Microsoft アカウントを持っていない場合は、無料のアカウントを取得するためのオプションがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="02621-110">If you don't have a Microsoft account, there are a couple of options to get a free account:</span></span>

- <span data-ttu-id="02621-111">[新しい個人用 Microsoft アカウントにサインアップ](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1)することができます。</span><span class="sxs-lookup"><span data-stu-id="02621-111">You can [sign up for a new personal Microsoft account](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1).</span></span>
- <span data-ttu-id="02621-112">[Office 365 開発者プログラムにサインアップ](https://developer.microsoft.com/office/dev-program)して、無料の office 365 サブスクリプションを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="02621-112">You can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

## <a name="register-a-web-application-with-the-azure-active-directory-admin-center"></a><span data-ttu-id="02621-113">Web アプリケーションを Azure Active Directory 管理センターに登録する</span><span class="sxs-lookup"><span data-stu-id="02621-113">Register a web application with the Azure Active Directory admin center</span></span>

1. <span data-ttu-id="02621-114">ブラウザーを開き、[Azure Active Directory 管理センター](https://aad.portal.azure.com)へ移動します。</span><span class="sxs-lookup"><span data-stu-id="02621-114">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com).</span></span> <span data-ttu-id="02621-115">**個人用アカウント** (別名: Microsoft アカウント)、または**職場/学校アカウント**を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="02621-115">Login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="02621-116">左側のナビゲーションで **[Azure Active Directory]** を選択し、それから **[管理]** で **[アプリの登録]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02621-116">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

    ![<span data-ttu-id="02621-117">アプリの登録のスクリーンショット</span><span class="sxs-lookup"><span data-stu-id="02621-117">A screenshot of the App registrations</span></span> ](/tutorial/images/aad-portal-app-registrations.png)

1. <span data-ttu-id="02621-118">**[新規登録]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02621-118">Select **New registration**.</span></span> <span data-ttu-id="02621-119">**[アプリケーションを登録]** ページで、次のように値を設定します。</span><span class="sxs-lookup"><span data-stu-id="02621-119">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="02621-120">`Angular Graph Tutorial` に **[名前]** を設定します。</span><span class="sxs-lookup"><span data-stu-id="02621-120">Set **Name** to `Angular Graph Tutorial`.</span></span>
    - <span data-ttu-id="02621-121">**[サポートされているアカウントの種類]** を **[任意の組織のディレクトリ内のアカウントと個人用の Microsoft アカウント]** に設定します。</span><span class="sxs-lookup"><span data-stu-id="02621-121">Set **Supported account types** to **Accounts in any organizational directory and personal Microsoft accounts**.</span></span>
    - <span data-ttu-id="02621-122">**[リダイレクト URI]** で、最初のドロップダウン リストを `Web` に設定し、それから `http://localhost:4200` に値を設定します。</span><span class="sxs-lookup"><span data-stu-id="02621-122">Under **Redirect URI**, set the first drop-down to `Web` and set the value to `http://localhost:4200`.</span></span>

    ![[アプリケーションを登録する] ページのスクリーンショット](/tutorial/images/aad-register-an-app.png)

1. <span data-ttu-id="02621-124">**[登録]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02621-124">Choose **Register**.</span></span> <span data-ttu-id="02621-125">[**角度グラフのチュートリアル**] ページで、**アプリケーション (クライアント) ID**の値をコピーして保存します。次の手順で必要になります。</span><span class="sxs-lookup"><span data-stu-id="02621-125">On the **Angular Graph Tutorial** page, copy the value of the **Application (client) ID** and save it, you will need it in the next step.</span></span>

    ![新しいアプリ登録のアプリケーション ID のスクリーンショット](/tutorial/images/aad-application-id.png)

1. <span data-ttu-id="02621-127">**[管理]** の下の **[認証]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02621-127">Select **Authentication** under **Manage**.</span></span> <span data-ttu-id="02621-128">暗黙的な**grant**セクションを見つけ、**アクセストークン**と**ID トークン**を有効にします。</span><span class="sxs-lookup"><span data-stu-id="02621-128">Locate the **Implicit grant** section and enable **Access tokens** and **ID tokens**.</span></span> <span data-ttu-id="02621-129">**[保存]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02621-129">Choose **Save**.</span></span>

    ![[暗黙的な許可] セクションのスクリーンショット](/tutorial/images/aad-implicit-grant.png)

## <a name="configure-the-sample"></a><span data-ttu-id="02621-131">サンプルを構成する</span><span class="sxs-lookup"><span data-stu-id="02621-131">Configure the sample</span></span>

1. <span data-ttu-id="02621-132">ファイルの`oauth.ts.example`名前を`oauth.ts`に変更します。</span><span class="sxs-lookup"><span data-stu-id="02621-132">Rename the `oauth.ts.example` file to `oauth.ts`.</span></span>
1. <span data-ttu-id="02621-133">`oauth.ts`ファイルを編集し、次のように変更します。</span><span class="sxs-lookup"><span data-stu-id="02621-133">Edit the `oauth.ts` file and make the following changes.</span></span>
    1. <span data-ttu-id="02621-134">を`YOUR_APP_ID_HERE`アプリ登録ポータルで取得した**アプリケーション Id**に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="02621-134">Replace `YOUR_APP_ID_HERE` with the **Application Id** you got from the App Registration Portal.</span></span>
1. <span data-ttu-id="02621-135">コマンドラインインターフェイス (CLI) で、このディレクトリに移動し、次のコマンドを実行して要件をインストールします。</span><span class="sxs-lookup"><span data-stu-id="02621-135">In your command-line interface (CLI), navigate to this directory and run the following command to install requirements.</span></span>

    ```Shell
    npm install
    ```

## <a name="run-the-sample"></a><span data-ttu-id="02621-136">サンプルを実行する</span><span class="sxs-lookup"><span data-stu-id="02621-136">Run the sample</span></span>

1. <span data-ttu-id="02621-137">CLI で次のコマンドを実行して、アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="02621-137">Run the following command in your CLI to start the application.</span></span>

    ```Shell
    ng serve
    ```

1. <span data-ttu-id="02621-138">Web ブラウザーを開き、`http://localhost:4200` を参照します。</span><span class="sxs-lookup"><span data-stu-id="02621-138">Open a browser and browse to `http://localhost:4200`.</span></span>