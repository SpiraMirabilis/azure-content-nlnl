<properties
	pageTitle="Tutorial: Azure Active Directory integration with The Funding Portal | Microsoft Azure"
	description="Learn how to configure single sign-on between Azure Active Directory and The Funding Portal."
	services="active-directory"
	documentationCenter=""
	authors="jeevansd"
	manager="femila"
	editor=""/>

<tags
	ms.service="active-directory"
	ms.workload="identity"
	ms.tgt_pltfrm="na"
	ms.devlang="na"
	ms.topic="article"
	ms.date="09/02/2016"
	ms.author="jeedes"/>


# Tutorial: Azure Active Directory integration with The Funding Portal

In this tutorial, you learn how to integrate The Funding Portal with Azure Active Directory (Azure AD).

Integrating The Funding Portal with Azure AD provides you with the following benefits:

- You can control in Azure AD who has access to The Funding Portal
- You can enable your users to automatically get signed-on to The Funding Portal (Single Sign-On) with their Azure AD accounts
- You can manage your accounts in one central location - the Azure classic portal

If you want to know more details about SaaS app integration with Azure AD, see [What is application access and single sign-on with Azure Active Directory](active-directory-appssoaccess-whatis.md).

## Prerequisites

To configure Azure AD integration with The Funding Portal, you need the following items:

- An Azure AD subscription
- A **The Funding Portal** single-sign on enabled subscription


> [AZURE.NOTE] To test the steps in this tutorial, we do not recommend using a production environment.


To test the steps in this tutorial, you should follow these recommendations:

- You should not use your production environment, unless this is necessary.
- If you don't have an Azure AD trial environment, you can get a one-month trial [here](https://azure.microsoft.com/pricing/free-trial/).


## Scenario description
In this tutorial, you test Azure AD single sign-on in a test environment. 
The scenario outlined in this tutorial consists of two main building blocks:

1. Adding The Funding Portal from the gallery
2. Configuring and testing Azure AD single sign-on


## Adding The Funding Portal from the gallery
To configure the integration of The Funding Portal into Azure AD, you need to add The Funding Portal from the gallery to your list of managed SaaS apps.

**To add The Funding Portal from the gallery, perform the following steps:**

1. In the **Azure classic portal**, on the left navigation pane, click **Active Directory**. 

	![Active Directory][1]

2. From the **Directory** list, select the directory for which you want to enable directory integration.

3. To open the applications view, in the directory view, click **Applications** in the top menu.

	![Applications][2]

4. Click **Add** at the bottom of the page.

	![Applications][3]

5. On the **What do you want to do** dialog, click **Add an application from the gallery**.

	![Applications][4]

6. In the search box, type **The Funding Portal**.

	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/tutorial_thefundingportal_01.png)

7. In the results pane, select **The Funding Portal**, and then click **Complete** to add the application.

	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/tutorial_thefundingportal_02.png)

##  Configuring and testing Azure AD single sign-on
In this section, you configure and test Azure AD single sign-on with The Funding Portal based on a test user called "Britta Simon".

For single sign-on to work, Azure AD needs to know what the counterpart user in The Funding Portal is to a user in Azure AD. In other words, a link relationship between an Azure AD user and the related user in The Funding Portal needs to be established.
This link relationship is established by assigning the value of the **user name** in Azure AD as the value of the **Username** in The Funding Portal.

To configure and test Azure AD single sign-on with The Funding Portal, you need to complete the following building blocks:

1. **[Configuring Azure AD Single Sign-On](#configuring-azure-ad-single-single-sign-on)** - to enable your users to use this feature.
2. **[Creating an Azure AD test user](#creating-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
4. **[Creating a The Funding Portal test user](#creating-a-the-funding-portal-test-user)** - to have a counterpart of Britta Simon in The Funding Portal that is linked to the Azure AD representation of her.
5. **[Assigning the Azure AD test user](#assigning-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Testing Single Sign-On](#testing-single-sign-on)** - to verify whether the configuration works.

### Configuring Azure AD single sign-on

The objective of this section is to enable Azure AD single sign-on in the Azure classic portal and to configure single sign-on in your The Funding Portal application.

The Funding Portal application expects the SAML assertions to contain an attribute named "externalId1". The value of "externalId1" should be a recognized studentID. Please configure the "externalId1" claim for this application. You can manage the values of these attributes from the **"Atrributes"** tab of the application. The following screenshot shows an example for this.

![Configure Single Sign-On](./media/active-directory-saas-thefundingportal-tutorial/tutorial_thefundingportal_03.png) 

**To configure Azure AD single sign-on with The Funding Portal, perform the following steps:**

1. In the Azure classic portal, on the **The Funding Portal** application integration page, in the menu on the top, click **Attributes**.
     
    ![Configure Single Sign-On][5]

2. On the SAML token attributes dialog, add the "externalId1" attribute.

	a. Click **add user attribute** to open the **Add User Attribute** dialog. 
	
	![Configure Single Sign-On](./media/active-directory-saas-thefundingportal-tutorial/tutorial_thefundingportal_05.png)

	b. In the **Attribute Name** textbox, type the attribute name "externalId1".

	c. From the **Attribute Value** list, select the attribute you want to use for your implementation. For example, if you have stored the StudentID value in the ExtensionAttribute1, then select user.extensionattribute1.

	d. Click **Complete**. Then, click **Apply Changes**.

1. In the menu on the top, click **Quick Start**.

	![Configure Single Sign-On][6]

2. In the classic portal, on the **The Funding Portal** application integration page, click **Configure single sign-on** to open the **Configure Single Sign-On**  dialog.

	![Configure Single Sign-On][7] 

3. On the **How would you like users to sign on to The Funding Portal** page, select **Azure AD Single Sign-On**, and then click **Next**.
 	
	![Configure Single Sign-On](./media/active-directory-saas-thefundingportal-tutorial/tutorial_thefundingportal_06.png)

4. On the **Configure App Settings** dialog page, perform the following steps: 

	![Configure Single Sign-On](./media/active-directory-saas-thefundingportal-tutorial/tutorial_thefundingportal_07.png)


    a. In the Sign On URL text box, type a URL using the following pattern: `https://<subdomain>.regenteducation.net/`.

	b. Click **Next**.

5. On the **Configure single sign-on at The Funding Portal** page, Click **Download metadata**, and then save the file on your computer.

	![Configure Single Sign-On](./media/active-directory-saas-thefundingportal-tutorial/tutorial_thefundingportal_08.png)

6. To get SSO configured for your application, contact The Funding Portal support. They will assist with the proper channel to configure SSO. Please note that you have to send email and attach downloaded metadata file to info@regenteducation.com.

7. In the classic portal, select the single sign-on configuration confirmation, and then click **Next**.
	
	![Azure AD Single Sign-On][10]

8. On the **Single sign-on confirmation** page, click **Complete**.  
  	
	![Azure AD Single Sign-On][11]

### Creating an Azure AD test user
In this section, you create a test user in the classic portal called Britta Simon.

![Create Azure AD User][20]

**To create a test user in Azure AD, perform the following steps:**

1. In the **Azure classic portal**, on the left navigation pane, click **Active Directory**.
	
	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/create_aaduser_09.png) 

2. From the **Directory** list, select the directory for which you want to enable directory integration.

3. To display the list of users, in the menu on the top, click **Users**.
	
	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/create_aaduser_03.png) 

4. To open the **Add User** dialog, in the toolbar on the bottom, click **Add User**.

	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/create_aaduser_04.png) 

5. On the **Tell us about this user** dialog page, perform the following steps:
 
	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/create_aaduser_05.png) 

    a. As Type Of User, select New user in your organization.

    b. In the User Name **textbox**, type **BrittaSimon**.

    c. Click **Next**.

6.  On the **User Profile** dialog page, perform the following steps:

	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/create_aaduser_06.png) 

    a. In the **First Name** textbox, type **Britta**.  

    b. In the **Last Name** textbox, type, **Simon**.

    c. In the **Display Name** textbox, type **Britta Simon**.

    d. In the **Role** list, select **User**.

    e. Click **Next**.

7. On the **Get temporary password** dialog page, click **create**.

	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/create_aaduser_07.png) 

8. On the **Get temporary password** dialog page, perform the following steps:

	![Creating an Azure AD test user](./media/active-directory-saas-thefundingportal-tutorial/create_aaduser_08.png) 

    a. Write down the value of the **New Password**.

    b. Click **Complete**.   



### Creating a The Funding Portal test user

In this section, you create a user called Britta Simon in The Funding Portal. If you don't know how to add Britta Simon in The Funding Portal, please work with The Funding Portal support team to add the test user and enable SSO. Contact them at info@regenteducation.com.

### Assigning the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting her access to The Funding Portal.

![Assign User][200] 

**To assign Britta Simon to The Funding Portal, perform the following steps:**

1. On the classic portal, to open the applications view, in the directory view, click **Applications** in the top menu.

	![Assign User][201] 

2. In the applications list, select **The Funding Portal**.

	![Configure Single Sign-On](./media/active-directory-saas-thefundingportal-tutorial/tutorial_thefundingportal_09.png) 

1. In the menu on the top, click **Users**.

	![Assign User][203] 

1. In the All Users list, select **Britta Simon**.

2. In the toolbar on the bottom, click **Assign**.

	![Assign User][205]


### Testing single sign-on

The objective of this section is to test your Azure AD single sign-on configuration using the Access Panel.

When you click the The Funding Portal tile in the Access Panel, you should get automatically signed-on to your The Funding Portal application.

## Additional resources

* [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](active-directory-saas-tutorial-list.md)
* [What is application access and single sign-on with Azure Active Directory?](active-directory-appssoaccess-whatis.md)



<!--Image references-->

[1]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_04.png


[5]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_05.png
[6]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_06.png
[7]:  ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_050.png
[10]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_060.png
[11]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_070.png
[20]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_201.png
[203]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_203.png
[204]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_204.png
[205]: ./media/active-directory-saas-thefundingportal-tutorial/tutorial_general_205.png