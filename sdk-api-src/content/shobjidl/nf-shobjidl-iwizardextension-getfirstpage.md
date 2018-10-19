---
UID: NF:shobjidl.IWizardExtension.GetFirstPage
title: IWizardExtension::GetFirstPage
author: windows-sdk-content
description: Gets a handle to the first page of the wizard extension.
old-location: shell\IWizardExtension_GetFirstPage.htm
tech.root: shell
ms.assetid: 1276b63d-6d5e-4e60-b936-b307cd922b4b
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetFirstPage, GetFirstPage method [Windows Shell], GetFirstPage method [Windows Shell],IWizardExtension interface, IWizardExtension interface [Windows Shell],GetFirstPage method, IWizardExtension.GetFirstPage, IWizardExtension::GetFirstPage, _shell_IWizardExtension_GetFirstPage, shell.IWizardExtension_GetFirstPage, shobjidl/IWizardExtension::GetFirstPage
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
 - IWizardExtension.GetFirstPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWizardExtension::GetFirstPage


## -description


Gets a handle to the first page of the wizard extension.


## -parameters




### -param phpage

TBD




#### - phPage [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to a <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> handle representing the first page of any wizard extension pages.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Although the wizard extension may host several sequential HTML pages, if it consists of only one page, the handles returned by <b>IWizardExtension::GetFirstPage</b> and <a href="https://msdn.microsoft.com/b4fc1089-d0fb-406d-bf05-b43b3f2cc87e">IWizardExtension::GetLastPage</a> are the same.
      




## -see-also




<a href="https://msdn.microsoft.com/f2d69f18-73de-44c1-9543-909e509b1c4f">IWizardExtension</a>



<a href="https://msdn.microsoft.com/b4fc1089-d0fb-406d-bf05-b43b3f2cc87e">IWizardExtension::GetLastPage</a>
 

 

