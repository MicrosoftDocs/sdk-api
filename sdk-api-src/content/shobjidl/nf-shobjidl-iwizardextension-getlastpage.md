---
UID: NF:shobjidl.IWizardExtension.GetLastPage
title: IWizardExtension::GetLastPage (shobjidl.h)
description: Gets a handle to the final page of the wizard extension pages.
helpviewer_keywords: ["GetLastPage","GetLastPage method [Windows Shell]","GetLastPage method [Windows Shell]","IWizardExtension interface","IWizardExtension interface [Windows Shell]","GetLastPage method","IWizardExtension.GetLastPage","IWizardExtension::GetLastPage","_shell_IWizardExtension_GetLastPage","shell.IWizardExtension_GetLastPage","shobjidl/IWizardExtension::GetLastPage"]
old-location: shell\IWizardExtension_GetLastPage.htm
tech.root: shell
ms.assetid: b4fc1089-d0fb-406d-bf05-b43b3f2cc87e
ms.date: 12/05/2018
ms.keywords: GetLastPage, GetLastPage method [Windows Shell], GetLastPage method [Windows Shell],IWizardExtension interface, IWizardExtension interface [Windows Shell],GetLastPage method, IWizardExtension.GetLastPage, IWizardExtension::GetLastPage, _shell_IWizardExtension_GetLastPage, shell.IWizardExtension_GetLastPage, shobjidl/IWizardExtension::GetLastPage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWizardExtension::GetLastPage
 - shobjidl/IWizardExtension::GetLastPage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IWizardExtension.GetLastPage
---

# IWizardExtension::GetLastPage


## -description

Gets a handle to the final page of the wizard extension pages.

## -parameters

### -param phpage [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to a <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> handle representing the wizard extension's final page.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This value is used to navigate backward into the wizard extension pages when the user clicks the <b>Back</b> button.
      

Although the wizard extension may host several sequential HTML pages, if it consists of only one page the handles returned by <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iwizardextension-getfirstpage">IWizardExtension::GetFirstPage</a> and <b>IWizardExtension::GetLastPage</b> are the same.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iwizardextension">IWizardExtension</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-iwizardextension-getfirstpage">IWizardExtension::GetFirstPage</a>