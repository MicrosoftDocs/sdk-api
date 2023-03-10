---
UID: NF:shobjidl_core.IShellPropSheetExt.ReplacePage
title: IShellPropSheetExt::ReplacePage (shobjidl_core.h)
description: Replaces a page in a property sheet for a Control Panel object.
helpviewer_keywords: ["IShellPropSheetExt interface [Windows Shell]","ReplacePage method","IShellPropSheetExt.ReplacePage","IShellPropSheetExt::ReplacePage","ReplacePage","ReplacePage method [Windows Shell]","ReplacePage method [Windows Shell]","IShellPropSheetExt interface","_win32_IShellPropSheetExt_ReplacePage","_win32_ishellpropsheetext_win32_ishellpropsheetext_replacepage_cpp","shell.IShellPropSheetExt_ReplacePage","shobjidl_core/IShellPropSheetExt::ReplacePage"]
old-location: shell\IShellPropSheetExt_ReplacePage.htm
tech.root: shell
ms.assetid: 0addd55c-756e-41f6-998e-0f464b609aac
ms.date: 12/05/2018
ms.keywords: IShellPropSheetExt interface [Windows Shell],ReplacePage method, IShellPropSheetExt.ReplacePage, IShellPropSheetExt::ReplacePage, ReplacePage, ReplacePage method [Windows Shell], ReplacePage method [Windows Shell],IShellPropSheetExt interface, _win32_IShellPropSheetExt_ReplacePage, _win32_ishellpropsheetext_win32_ishellpropsheetext_replacepage_cpp, shell.IShellPropSheetExt_ReplacePage, shobjidl_core/IShellPropSheetExt::ReplacePage
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellPropSheetExt::ReplacePage
 - shobjidl_core/IShellPropSheetExt::ReplacePage
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
 - IShellPropSheetExt.ReplacePage
---

# IShellPropSheetExt::ReplacePage


## -description

Replaces a page in a property sheet for a Control Panel object.

## -parameters

### -param uPageID

Type: <b>UINT</b>

Not used.

<b>Microsoft Windows XP and earlier:</b> A type EXPPS identifier of the page to replace. The values for this parameter for Control Panels can be found in the Cplext.h header file.

### -param pfnReplaceWith [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to a function that the property sheet handler calls to replace a page to the property sheet. The function takes a property sheet handle returned by the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function and the <i>lParam</i> parameter passed to the <b>ReplacePage</b> method.

### -param lParam [in]

Type: <b>LPARAM</b>

The parameter to pass to the function specified by the <i>pfnReplacePage</i> parameter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To replace a page, a property sheet handler fills a <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure, calls <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a>, and then calls the function specified by <i>pfnReplacePage</i>.