# Blazor Web Application

This is a Blazor web application that serves as a simple example of a multi-page web application. It consists of a home page, a contact page, and includes features such as navigation, form validation, and user authentication.

## Purpose

The purpose of this application is to demonstrate the following:

- Creating a multi-page web application using Blazor.
- Implementing navigation between pages with a navigation bar or menu.
- Displaying content on the home page to introduce Blazor and its advantages.
- Creating a contact page with a feedback form for collecting user feedback.
- Implementing form validation to ensure the correctness of user inputs.
- Adding user login functionality to access specific pages.
- Auto-populating user information on the contact page for a personalized experience.

## Features

- **Home Page:** Provides an introduction to Blazor and its advantages.

- **Contact Page:** Allows users to submit feedback via a form with fields for name, email, and message. Form validation ensures that the email field follows the correct format.

- **Navigation:** A navigation bar or menu facilitates seamless navigation between the home and contact pages.

- **Login Functionality:** Users can log in to access specific features or personalized information on the contact page. Note that this application does not currently have a database, but you can develop the login functionality using SQL for user authentication and data storage.

### Sample SQL Connection Code

To implement user authentication and data storage using SQL, you can use technologies such as Entity Framework Core. Here's a sample code snippet for establishing a SQL Server connection:

```csharp
using Microsoft.Data.SqlClient;

public class SqlDatabase
{
    private readonly string _connectionString;

    public SqlDatabase(string connectionString)
    {
        _connectionString = connectionString;
    }

    public SqlConnection OpenConnection()
    {
        var connection = new SqlConnection(_connectionString);
        connection.Open();
        return connection;
    }
}
## Deployment on Azure

This Blazor web application is hosted on Microsoft Azure, a cloud computing platform. It is published directly from Visual Studio, making deployment quick and straightforward. Below are the steps to deploy your own instance of this application on Azure:

### Prerequisites

Before you begin, ensure that you have the following:

1. **Azure Account:** If you don't have one, you can sign up for a free Azure account at [azure.com](https://azure.com).

2. **Visual Studio:** Ensure that you have Visual Studio installed and configured for use with Azure.

### Deployment Steps

1. **Azure App Service:** This application is hosted on Azure App Service, which is a platform for building, deploying, and scaling web apps. Follow these steps to create an Azure App Service for your Blazor app:

   - In Visual Studio, right-click on your Blazor project in Solution Explorer.

   - Select "Publish" to open the Publish dialog.

   - Choose "Azure" as the target.

   - Sign in to your Azure account if prompted.

   - Create a new Azure App Service (replace `<app-service-name>` and `<resource-group-name>` with your preferred values).

   - Configure any additional settings as needed, such as the Azure region and pricing tier.

   - Click "Create" to create the Azure App Service.

2. **Deployment:** Deploy your Blazor app to Azure App Service directly from Visual Studio:

   - In the Publish dialog, select the Azure App Service you created in the previous step.

   - Click "Publish" to deploy your application to Azure.

   - Visual Studio will build and deploy your Blazor app to Azure App Service automatically.

3. **Access Your Deployed Application:**

   - After the deployment is complete, you can access your deployed Blazor application using the URL provided by Azure App Service (e.g., `https://<app-service-name>.azurewebsites.net`).

Now your Blazor application is deployed and hosted on Microsoft Azure, directly published from Visual Studio, and ready for users to access.

**Note:** Azure offers various hosting options, and this deployment method uses Azure App Service for its simplicity and seamless integration with Visual Studio.


## Technologies Used

- [Blazor](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor): A framework for building interactive web applications using C# and .NET.

- [C#](https://docs.microsoft.com/en-us/dotnet/csharp/): The programming language used for server-side logic in Blazor.

- [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML): Used for defining the structure of web pages.

- [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS): Used for styling the web application.

- [ASP.NET Core](https://dotnet.microsoft.com/apps/aspnet): The underlying web framework for hosting Blazor applications.

- [Authentication and Authorization](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/): Used for implementing login functionality.

## Getting Started

To run this application locally or contribute to it, follow these steps:

1. Clone the repository to your local machine.
   ```bash
   git clone https://github.com/yourusername/your-blazor-app.git
