---
UID: NN:shobjidl.IPublishingWizard
title: IPublishingWizard
author: windows-sdk-content
description: Exposes methods for working with the Online Print Wizard, the Web Publishing Wizard, and the Add Network Place Wizard. In Windows Vista, IPublishingWizard no longer supports the Web Publishing Wizard or Online Print Wizard.
old-location: shell\IPublishingWizard.htm
tech.root: shell
ms.assetid: 634dcc04-e2ed-4cde-bb4d-d2e8bcf5ab94
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IPublishingWizard, IPublishingWizard interface [Windows Shell], IPublishingWizard interface [Windows Shell],described, _shell_IPublishingWizard, shell.IPublishingWizard, shobjidl/IPublishingWizard
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IPublishingWizard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPublishingWizard interface


## -description


Exposes methods for working with the Online Print Wizard, the Web Publishing Wizard, and the Add Network Place Wizard. In Windows Vista, <b>IPublishingWizard</b> no longer supports the Web Publishing Wizard or Online Print Wizard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPublishingWizard</b> interface inherits from <a href="https://msdn.microsoft.com/f2d69f18-73de-44c1-9543-909e509b1c4f">IWizardExtension</a>. <b>IPublishingWizard</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPublishingWizard</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c595526-f810-4a33-82c3-785727153b16">GetTransferManifest</a>
</td>
<td align="left" width="63%">
Gets a transfer manifest for a file transfer operation performed by a publishing wizard, such as the Online Print Wizard or the Add Network Place Wizard.  
    
                        

<div class="alert"><b>Note</b>  This method is deprecated for Windows Vista, as it is not supported for Online Print Wizard or Add Network Place Wizard.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8312bb2e-cc06-4440-a72c-cf153a5d61b6">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the <a href="https://msdn.microsoft.com/e96a2721-0d00-4b83-8f78-46f6356f77e2">Publishing Wizard</a> object with the files to transfer, the settings to use, and the type of wizard to create.
    			
                        

<div class="alert"><b>Note</b>  Windows Vista no longer supports the Online Print Wizard. However, this method can still be used to generate the Add Network Place Wizard.</div>
<div> </div>
</td>
</tr>
</table> 


## -remarks



The Online Print Wizard is a wizard for ordering prints of photos online. The use of <b>IPublishingWizard</b> to work with the Online Print Wizard is no longer supported in Windows Vista.

The Add Network Place Wizard allows the user to create a shortcut to network resources in My Network Places (in Windows XP) or Computer (in Windows Vista).

The Windows Shell supplies a <a href="https://msdn.microsoft.com/e96a2721-0d00-4b83-8f78-46f6356f77e2">Publishing Wizard object</a> that implements <b>IPublishingWizard</b> and <a href="https://msdn.microsoft.com/f2d69f18-73de-44c1-9543-909e509b1c4f">IWizardExtension</a>. The methods of <b>IPublishingWizard</b> are used to initialize the type of the wizard, set certain attributes of the wizard, and retrieve a transfer manifest. The methods of <b>IWizardExtension</b> are used to retrieve the extension pages that make up the body of the selected wizard. To instantiate the <b>Publishing Wizard object</b>, call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> and use the class identifier (CLSID) CLSID_PublishingWizard and IID_IPublishingWizard as the REFIID.


```cpp
IPublishingWizard *pPublish = NULL;

HRESULT hr = CoCreateInstance(CLSID_PublishingWizard, 
                              NULL,
                              CLSCTX_INPROC_SERVER, 
                              IID_IPublishingWizard, 
                              (LPVOID*)&pPublish);

```


Once the <a href="https://msdn.microsoft.com/e96a2721-0d00-4b83-8f78-46f6356f77e2">Publishing Wizard object</a> has been instantiated, call <a href="https://msdn.microsoft.com/8312bb2e-cc06-4440-a72c-cf153a5d61b6">IPublishingWizard::Initialize</a> to initialize the <b>Publishing Wizard object</b>.

<div class="alert"><b>Note</b>  The examples below will not work on Windows Vista since the <b>IPublishingWizard</b> methods no longer support the Online Printing Wizard in Windows Vista.</div>
<div> </div>

```cpp
// Initializing the Online Print Wizard
                    
hr = pPublish->Initialize(pDataObject,
                          SHPWHF_NOFILESELECTOR,
                          L"InternetPhotoPrinting");
                          
// pDataObject: A data object that represents files or folders to transfer.
// SHPWHF_NOFILESELECTOR: This flag must be set.
// L"InternetPhotoPrinting": Display the Online Print Wizard.

```


Note that <a href="https://msdn.microsoft.com/8312bb2e-cc06-4440-a72c-cf153a5d61b6">IPublishingWizard::Initialize</a> does not actually display the wizard. In order to display the Online Print Wizard, you must create a <a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PROPSHEETHEADER</a> structure and then modify its <i>phpage</i> member to include the array of <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> handles returned by <a href="https://msdn.microsoft.com/2d9a5012-3b5e-4e55-984b-70a932bab569">IWizardExtension::AddPages</a>. <b>IWizardExtension::AddPages</b> is implemented by the same <a href="https://msdn.microsoft.com/e96a2721-0d00-4b83-8f78-46f6356f77e2">Publishing Wizard object</a> that implements <b>IPublishingWizard</b>.

If displaying the Online Print Wizard, the PSH_NOMARGIN flag should be set in the <i>dwFlags</i> member of the <a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PROPSHEETHEADER</a> structure that contains the extension pages.

In addition to the extension pages retrieved from <a href="https://msdn.microsoft.com/2d9a5012-3b5e-4e55-984b-70a932bab569">IWizardExtension::AddPages</a>, the <i>phpage</i> array should include a start page, a cancel page, and a finish page, provided by your application. When the user backs out of or cancels the extension, or when the extension finishes displaying its pages, the extension then communicates to the wizard that it must navigate out of the stack of extension pages to one of these application-provided pages. Your application must supply an implementation of <a href="https://msdn.microsoft.com/4c366f9c-d774-4390-8f43-8c25f86e3c35">IWizardSite</a> that handles this communication. The <b>IPublishingWizard</b> object's site must be set to your <b>IWizardSite</b> implementation. The <a href="https://msdn.microsoft.com/66175435-f85b-4e26-b148-f4edb74cb41d">IUnknown_SetSite</a> function can be used to set the site. Once your application has specified the wizard settings using <a href="https://msdn.microsoft.com/8312bb2e-cc06-4440-a72c-cf153a5d61b6">IPublishingWizard::Initialize</a>, properly populated the <i>phpage</i> member of a <a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PROPSHEETHEADER</a> structure, and set the site to an implementation of <b>IWizardSite</b>, the wizard may be displayed by calling the <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function.


```cpp
/* This is example code demonstrating how to populate a PROPSHEETHEADER
structure and use it to display the Online Print Wizard.
This sample assumes that the PublishingWizard object has already
been instantiated and initialized elsewhere in the application. */

// Define the number of wizard pages that we expect to get from 
// the Publishing Wizard object. 
// The Online Print Wizard provides 6 predefined pages in Windows Vista,
// but provided 9 in Windows XP. 
#if NTDDI_VERSION >= NTDDI_VISTA
#define NUMPAGES 6  
#else
#define NUMPAGES 9
#endif

// Number of wizard pages supplied by the application in addition to 
// the predefined pages supplied by the Online Print Wizard. 
#define NUMNONEXTENSIONPAGES 3

// Array to hold the property sheets to display in the wizard,
// including both those returned by IPublishingWizard::AddPages()
// and those application-defined pages returned by IWizardSite methods.
HPROPSHEETPAGE hPropSheets[NUMPAGES + NUMNONEXTENSIONPAGES];

// Handles to the application-defined property sheets.
// This example assumes that they are initialized elsewhere in the application.
HPROPSHEETPAGE hPropSheetFinishPage = CreateFinishPage;
HPROPSHEETPAGE hPropSheetStartPage = CreateStartPage;
HPROPSHEETPAGE hPropSheetCanceledPage = CreateCanceledPage;

// Number of property sheets returned by IPublishingWizard::AddPages().
UINT uCount = 0;
INT_PTR retval = 0; // return value from PropertySheet
HRESULT hr;

// Property sheet header structure whose phpage member will receive
// the array of wizard pages retrieved from AddPages.
PROPSHEETHEADER psh;
psh.dwSize = sizeof(PROPSHEETHEADER);

// Set the PublishingWizard object's site to an IWizardSite implementation
// defined by your application.  
hr = IUnknown_SetSite(pIPublish, (IUnknown *)pWizSite);

// Fill the hPropSheets array with the pages of the wizard.
if SUCCEEDED(hr)
{
    hr = pIPublish->AddPages(&hPropSheets[0], NUMPAGES, &uCount);
}        

if SUCCEEDED(hr)
{
    // Define start, finish, and canceled pages elsewhere in your application.
    // Here, these pages are added after the extension pages.
    hPropSheets[uCount] = hPropSheetFinishPage;
    hPropSheets[uCount + 1] = hPropSheetCanceledPage;
    hPropSheets[uCount + 2] = hPropSheetStartPage;

    // Assign the array of property sheets.
    psh.phpage = hPropSheets;

    // Number of extension pages from AddPages + # of your own pages.
    psh.nPages = uCount + NUMNONEXTENSIONPAGES; 

    // The index into phpage where the first page to display is located.
    psh.nStartPage = 0;  

    // PSH_NOMARGIN must be specified for the Online Print Wizard.
    psh.dwFlags =  PSH_AEROWIZARD | PSH_WIZARD | PSH_NOMARGIN;
    psh.hwndParent = NULL;
    psh.hInstance = NULL;

    // Display the wizard.
    PropertySheet(&psh);
}

```





## -see-also




<a href="https://msdn.microsoft.com/f2d69f18-73de-44c1-9543-909e509b1c4f">IWizardExtension</a>



<a href="https://msdn.microsoft.com/2d9a5012-3b5e-4e55-984b-70a932bab569">IWizardExtension::AddPages</a>



<a href="https://msdn.microsoft.com/4c366f9c-d774-4390-8f43-8c25f86e3c35">IWizardSite</a>



<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PROPSHEETHEADER</a>



<a href="https://msdn.microsoft.com/e96a2721-0d00-4b83-8f78-46f6356f77e2">Publishing Wizard object</a>
 

 

