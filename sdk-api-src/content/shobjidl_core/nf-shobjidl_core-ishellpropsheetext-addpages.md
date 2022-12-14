---
UID: NF:shobjidl_core.IShellPropSheetExt.AddPages
title: IShellPropSheetExt::AddPages (shobjidl_core.h)
description: Adds one or more pages to a property sheet that the Shell displays for a file object. The Shell calls this method for each property sheet handler registered to the file type.
helpviewer_keywords: ["AddPages","AddPages method [Windows Shell]","AddPages method [Windows Shell]","IShellPropSheetExt interface","IShellPropSheetExt interface [Windows Shell]","AddPages method","IShellPropSheetExt.AddPages","IShellPropSheetExt::AddPages","_win32_IShellPropSheetExt_AddPages","_win32_ishellpropsheetext_win32_ishellpropsheetext_addpages_cpp","shell.IShellPropSheetExt_AddPages","shobjidl_core/IShellPropSheetExt::AddPages"]
old-location: shell\IShellPropSheetExt_AddPages.htm
tech.root: shell
ms.assetid: 76a2a94b-b79f-41d1-9e42-fbfda545d12f
ms.date: 12/05/2018
ms.keywords: AddPages, AddPages method [Windows Shell], AddPages method [Windows Shell],IShellPropSheetExt interface, IShellPropSheetExt interface [Windows Shell],AddPages method, IShellPropSheetExt.AddPages, IShellPropSheetExt::AddPages, _win32_IShellPropSheetExt_AddPages, _win32_ishellpropsheetext_win32_ishellpropsheetext_addpages_cpp, shell.IShellPropSheetExt_AddPages, shobjidl_core/IShellPropSheetExt::AddPages
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
 - IShellPropSheetExt::AddPages
 - shobjidl_core/IShellPropSheetExt::AddPages
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
 - IShellPropSheetExt.AddPages
---

# IShellPropSheetExt::AddPages


## -description

Adds one or more pages to a property sheet that the Shell displays for a file object. The Shell calls this method for each property sheet handler registered to the file type.

## -parameters

### -param pfnAddPage [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to a function that the property sheet handler calls to add a page to the property sheet. The function takes a property sheet handle returned by the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function and the <i>lParam</i> parameter passed to this method.

### -param lParam [in]

Type: <b>LPARAM</b>

Handler-specific data to pass to the function pointed to by <i>pfnAddPage</i>.

## -returns

Type: <b>HRESULT</b>

If successful, returns a one-based index to specify the page that should be initially displayed. See Remarks for more information.

## -remarks

For each page that the property sheet handler needs to add to a property sheet, the handler fills a <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure, calls the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function, and then calls the function pointed to by <i>pfnAddPage</i>.

The <b>LPFNADDPROPSHEETPAGE</b> function pointer type is defined in Prsht.h as shown here. It accepts a handle to a <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure and function-defined data through <i>lParam</i>.

                


``` syntax
typedef BOOL (* LPFNADDPROPSHEETPAGE)(HPROPSHEETPAGE, LPARAM);
```

You can request through your implementation that a particular property sheet page be displayed first, instead of the default page. To do so, return the one-based index of the desired page relative to the pages you added. For example, if you added three property sheet pages, A, B, and C, and you want B to be the selected page, then the return value should be 2. Note that this return value is only a request. The property sheet might still display the default page.
