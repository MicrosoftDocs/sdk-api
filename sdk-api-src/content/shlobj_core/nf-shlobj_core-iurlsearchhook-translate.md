---
UID: NF:shlobj_core.IURLSearchHook.Translate
title: IURLSearchHook::Translate (shlobj_core.h)
description: Called by the browser when the browser cannot determine the protocol of a URL address.
helpviewer_keywords: ["IURLSearchHook interface [Windows Shell]","Translate method","IURLSearchHook.Translate","IURLSearchHook::Translate","Translate","Translate method [Windows Shell]","Translate method [Windows Shell]","IURLSearchHook interface","_win32_IURLSearchHook_Translate","shell.IURLSearchHook_Translate","shlobj_core/IURLSearchHook::Translate"]
old-location: shell\IURLSearchHook_Translate.htm
tech.root: shell
ms.assetid: 02fa8ee7-f9cb-4872-895c-7b3078391cc4
ms.date: 12/05/2018
ms.keywords: IURLSearchHook interface [Windows Shell],Translate method, IURLSearchHook.Translate, IURLSearchHook::Translate, Translate, Translate method [Windows Shell], Translate method [Windows Shell],IURLSearchHook interface, _win32_IURLSearchHook_Translate, shell.IURLSearchHook_Translate, shlobj_core/IURLSearchHook::Translate
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
 - IURLSearchHook::Translate
 - shlobj_core/IURLSearchHook::Translate
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
 - IURLSearchHook.Translate
---

# IURLSearchHook::Translate


## -description

Called by the browser when the browser cannot determine the protocol of a URL address.

## -parameters

### -param pwszSearchURL [out]

Type: <b>PWSTR</b>

The address of a wide character buffer that, on entry, contains the URL address for which the browser is trying to determine the protocol. On exit, this buffer contains the modified URL address if the method was successful. See the return value for more information.

### -param cchBufferSize

Type: <b>DWORD</b>

The size, in characters, of the buffer at <i>pwszSearchURL</i>.

## -returns

Type: <b>HRESULT</b>

This method must return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The URL address was completely translated. The <i>lpwszSearchURL</i> parameter contains the full URL address. The browser will not call any other URL Search Hooks and will attempt to browse to the modified address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The URL address has been partially processed, but further translation is still required. The <i>lpwszSearchURL</i> parameter contains the result of the processing. The browser will continue executing the rest of the URL Search Hooks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The URL address was not translated. The <i>lpwszSearchURL</i> parameter has not been modified. The browser will continue executing the rest of the URL Search Hooks.

</td>
</tr>
</table>

