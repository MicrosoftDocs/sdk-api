---
UID: NF:winstring.WindowsStringHasEmbeddedNull
title: WindowsStringHasEmbeddedNull function (winstring.h)
description: Indicates whether the specified string has embedded null characters.
helpviewer_keywords: ["WindowsStringHasEmbeddedNull","WindowsStringHasEmbeddedNull function [Windows Runtime]","winrt.windowsstringhasembeddednull","winstring/WindowsStringHasEmbeddedNull"]
old-location: winrt\windowsstringhasembeddednull.htm
tech.root: WinRT
ms.assetid: BE3B0198-C6D1-4F3C-A9E2-F186FB025DCE
ms.date: 12/05/2018
ms.keywords: WindowsStringHasEmbeddedNull, WindowsStringHasEmbeddedNull function [Windows Runtime], winrt.windowsstringhasembeddednull, winstring/WindowsStringHasEmbeddedNull
req.header: winstring.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WindowsStringHasEmbeddedNull
 - winstring/WindowsStringHasEmbeddedNull
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - winstring.h
 - API-MS-Win-Core-WinRT-String-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
 - WindowsStringHasEmbeddedNull
---

## -description

Indicates whether the specified string has embedded null characters.

## -parameters

### -param string

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The string to test for embedded null characters.

### -param hasEmbedNull

Type: [out] <b>BOOL*</b>

<b>TRUE</b> if <i>string</i> has one or more embedded null characters; otherwise, <b>FALSE</b>. <b>FALSE</b> if  <i>string</i> is <b>NULL</b> or the empty string.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

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
The test completed  successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>hasEmbedNull</i> is <b>NULL</b>.

</td>
</tr>
</table>

