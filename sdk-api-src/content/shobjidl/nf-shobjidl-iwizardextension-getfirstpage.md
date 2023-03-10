---
UID: NF:shobjidl.IWizardExtension.GetFirstPage
title: IWizardExtension::GetFirstPage (shobjidl.h)
description: Gets a handle to the first page of the wizard extension.
helpviewer_keywords: ["GetFirstPage","GetFirstPage method [Windows Shell]","GetFirstPage method [Windows Shell]","IWizardExtension interface","IWizardExtension interface [Windows Shell]","GetFirstPage method","IWizardExtension.GetFirstPage","IWizardExtension::GetFirstPage","_shell_IWizardExtension_GetFirstPage","shell.IWizardExtension_GetFirstPage","shobjidl/IWizardExtension::GetFirstPage"]
old-location: shell\IWizardExtension_GetFirstPage.htm
tech.root: shell
ms.assetid: 1276b63d-6d5e-4e60-b936-b307cd922b4b
ms.date: 12/05/2018
ms.keywords: GetFirstPage, GetFirstPage method [Windows Shell], GetFirstPage method [Windows Shell],IWizardExtension interface, IWizardExtension interface [Windows Shell],GetFirstPage method, IWizardExtension.GetFirstPage, IWizardExtension::GetFirstPage, _shell_IWizardExtension_GetFirstPage, shell.IWizardExtension_GetFirstPage, shobjidl/IWizardExtension::GetFirstPage
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
 - IWizardExtension::GetFirstPage
 - shobjidl/IWizardExtension::GetFirstPage
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
 - IWizardExtension.GetFirstPage
---

# IWizardExtension::GetFirstPage


## -description

Gets a handle to the first page of the wizard extension.

## -parameters

### -param phpage [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to a <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> handle representing the first page of any wizard extension pages.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Although the wizard extension may host several sequential HTML pages, if it consists of only one page, the handles returned by <b>IWizardExtension::GetFirstPage</b> and <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iwizardextension-getlastpage">IWizardExtension::GetLastPage</a> are the same.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iwizardextension">IWizardExtension</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-iwizardextension-getlastpage">IWizardExtension::GetLastPage</a>