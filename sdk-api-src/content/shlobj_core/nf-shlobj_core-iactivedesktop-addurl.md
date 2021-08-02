---
UID: NF:shlobj_core.IActiveDesktop.AddUrl
title: IActiveDesktop::AddUrl (shlobj_core.h)
description: Adds the desktop item associated with the specified URL.
helpviewer_keywords: ["AddUrl","AddUrl method [Legacy Windows Environment Features]","AddUrl method [Legacy Windows Environment Features]","IActiveDesktop interface","IActiveDesktop interface [Legacy Windows Environment Features]","AddUrl method","IActiveDesktop.AddUrl","IActiveDesktop::AddUrl","_win32_IActiveDesktop_AddUrl_Method","lwef.iactivedesktop_addurl_method","shell.iactivedesktop_addurl_method","shlobj_core/IActiveDesktop::AddUrl"]
old-location: lwef\iactivedesktop_addurl_method.htm
tech.root: lwef
ms.assetid: 295b2f46-6178-4aef-9721-8105c75a4a55
ms.date: 12/05/2018
ms.keywords: AddUrl, AddUrl method [Legacy Windows Environment Features], AddUrl method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],AddUrl method, IActiveDesktop.AddUrl, IActiveDesktop::AddUrl, _win32_IActiveDesktop_AddUrl_Method, lwef.iactivedesktop_addurl_method, shell.iactivedesktop_addurl_method, shlobj_core/IActiveDesktop::AddUrl
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActiveDesktop::AddUrl
 - shlobj_core/IActiveDesktop::AddUrl
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
 - IActiveDesktop.AddUrl
---

# IActiveDesktop::AddUrl


## -description

Adds the desktop item associated with the specified URL.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window for the user interface.

### -param pszSource [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the URL of the desktop item.

### -param pcomp [in]

Type: <b>LPCOMPONENT</b>

A pointer to the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure that contains the details of the desktop item to be added.

### -param dwFlags

Type: <b>DWORD</b>

An unsigned long integer value that controls this method. Can be set to ADDURL_SILENT to add a desktop item without displaying any user interfaces.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to add the desktop item or an instance of the desktop item already exists on the Active Desktop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVAILDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
If the ADDURL_SILENT flag has been set, the desktop item has either been added successfully or it already exists on the Active Desktop. Otherwise, the desktop item has been added successfully.

</td>
</tr>
</table>

## -remarks

By default, this method will display some user interface and then add the desktop item to the Active Desktop. Like <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem">IActiveDesktop::AddDesktopItem</a>, the client application must call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges">IActiveDesktop::ApplyChanges</a> to have the changes saved to the registry.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>



<a href="/windows/desktop/lwef/active-desktop-interface">Using the Active Desktop Object</a>