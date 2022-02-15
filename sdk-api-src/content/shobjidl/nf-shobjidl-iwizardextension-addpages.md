---
UID: NF:shobjidl.IWizardExtension.AddPages
title: IWizardExtension::AddPages (shobjidl.h)
description: Adds extension pages to the wizard by filling an array with handles to PROPSHEETPAGE structures representing those pages.
helpviewer_keywords: ["AddPages","AddPages method [Windows Shell]","AddPages method [Windows Shell]","IWizardExtension interface","IWizardExtension interface [Windows Shell]","AddPages method","IWizardExtension.AddPages","IWizardExtension::AddPages","_shell_IWizardExtension_AddPages","shell.IWizardExtension_AddPages","shobjidl/IWizardExtension::AddPages"]
old-location: shell\IWizardExtension_AddPages.htm
tech.root: shell
ms.assetid: 2d9a5012-3b5e-4e55-984b-70a932bab569
ms.date: 12/05/2018
ms.keywords: AddPages, AddPages method [Windows Shell], AddPages method [Windows Shell],IWizardExtension interface, IWizardExtension interface [Windows Shell],AddPages method, IWizardExtension.AddPages, IWizardExtension::AddPages, _shell_IWizardExtension_AddPages, shell.IWizardExtension_AddPages, shobjidl/IWizardExtension::AddPages
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
 - IWizardExtension::AddPages
 - shobjidl/IWizardExtension::AddPages
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
 - IWizardExtension.AddPages
---

# IWizardExtension::AddPages


## -description

Adds extension pages to the wizard by filling an array with handles to <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structures representing those pages.

## -parameters

### -param aPages [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to an array of <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> handles that represent the wizard dialog pages. Handles to <b>PROPSHEETPAGE</b> structures for the extension pages are added to this array.

### -param cPages [in]

Type: <b>UINT</b>

The count of elements in <i>aPages</i>.

### -param pnPagesAdded [out]

Type: <b>UINT*</b>

The count of handles successfully added.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The array of handles pointed to by <i>aPages</i> can contain handles to wizard dialog pages preceding and following the extension pages. The array's pointer should be passed to this method so that its value is the first empty array element, ready to accept the handle of the first extension page, rather than simply the first element. Collaterally, the value passed in <i>cPages</i> should state the number of unused array elements instead of the total number.

For example, if two introductory host pages were added to an array called <b>hpages</b>, then the call to <b>IWizardExtension::AddPages</b> would appear as follows.

				


```
#define ARRAYSIZE(a)    (sizeof(a)/sizeof(a[0]))
g_iwe->AddPages(&hpages[2], ARRAYSIZE(hpages)-2, &nPages);
```


Do not confuse wizard pages, which are <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structures, with hosted HTML pages. One wizard dialog page can host many sequential HTML pages. This method supplies the number of wizard dialog pages added by the wizard extension, not the number of server-side HTML pages which are displayed in it.