---
page_type: sample
description: This sample demonstrates how to use the Microsoft Graph .NET SDK to access data in Office 365 from Blazor WebAssembly apps.
products:
- ms-graph
- microsoft-graph-calendar-api
- office-exchange-online
- blazor
languages:
- csharp
---

This sample is built upon Microsoft Sample used to demonstrate on how to use the Microsoft Graph .NET SDK to access data in Office 365 from Blazor WebAssembly apps

# Microsoft Graph sample Blazor WebAssembly app

![License.](https://img.shields.io/badge/license-MIT-green.svg)


## Prerequisites

- [.NET Core SDK](https://dotnet.microsoft.com/download)

## Register an app in Azure AD

1. Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com). Login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.

1. Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.

1. Select **New registration**. On the **Register an application** page, set the values as follows.

    - Set **Name** to `Blazor Graph Sample`.
    - Set **Supported account types** to **Accounts in any organizational directory and personal Microsoft accounts**.
    - Under **Redirect URI**, set the first drop-down to **Single-page application (SPA)** and set the value to `https://localhost:7067/authentication/login-callback`.

1. Select **Register**. On the **Blazor Graph Tutorial** page, copy the value of the **Application (client) ID** and save it, you will need it in the next step.

## Configure the sample

1. Create a new file in the **./GraphSample/wwwroot** directory named **appsettings.Development.json** and add the following code.

    ```json
    {
      "AzureAd": {
        "ClientId": "YOUR_CLIENT_ID_HERE"
      }
    }
    ```

1. Replace `YOUR_CLIENT_ID_HERE` with the **Application (client) ID** value from your app registration.

## Running the sample

Run the following command in the **GraphSample** directory.

```dotnetcli
dotnet run
```

Open your browser to `https://localhost:7067`.


