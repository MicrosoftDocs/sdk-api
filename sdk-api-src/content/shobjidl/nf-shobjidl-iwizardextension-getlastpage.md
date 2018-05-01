---
UID: NF:shobjidl.IWizardExtension.GetLastPage
title: IWizardExtension::GetLastPage method
author: windows-driver-content
description: Gets a handle to the final page of the wizard extension pages.
old-location: shell\IWizardExtension_GetLastPage.htm
old-project: shell
ms.assetid: b4fc1089-d0fb-406d-bf05-b43b3f2cc87e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLastPage method [Windows Shell], GetLastPage method [Windows Shell], IWizardExtension interface, GetLastPage,IWizardExtension.GetLastPage, IWizardExtension, IWizardExtension interface [Windows Shell], GetLastPage method, IWizardExtension::GetLastPage, _shell_IWizardExtension_GetLastPage, shell.IWizardExtension_GetLastPage, shobjidl/IWizardExtension::GetLastPage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IWizardExtension.GetLastPage
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IWizardExtension::GetLastPage method


## -description


Gets a handle to the final page of the wizard extension pages.


## -parameters




### -param phpage






#### - phPage [out]

Type: <b>HPROPSHEETPAGE*</b>


          A pointer to a <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> handle representing the wizard extension's final page.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        This value is used to navigate backward into the wizard extension pages when the user clicks the <b>Back</b> button.
      


        Although the wizard extension may host several sequential HTML pages, if it consists of only one page the handles returned by <a href="https://msdn.microsoft.com/1276b63d-6d5e-4e60-b936-b307cd922b4b">IWizardExtension::GetFirstPage</a> and <b>IWizardExtension::GetLastPage</b> are the same.
      




## -see-also




<a href="https://msdn.microsoft.com/f2d69f18-73de-44c1-9543-909e509b1c4f">IWizardExtension</a>



<a href="https://msdn.microsoft.com/1276b63d-6d5e-4e60-b936-b307cd922b4b">IWizardExtension::GetFirstPage</a>
 

 

