---
UID: NF:winstring.HSTRING_UserUnmarshal
title: HSTRING_UserUnmarshal function (winstring.h)
description: The HSTRING_UserUnmarshal function (winstring.h) unmarshals an HSTRING object from the RPC buffer.
helpviewer_keywords: ["HSTRING_UserUnmarshal","HSTRING_UserUnmarshal function [Windows Runtime]","remotesystemadditionalinfo/HSTRING_UserUnmarshal","winrt.hstring_userunmarshal"]
old-location: winrt\hstring_userunmarshal.htm
tech.root: WinRT
ms.assetid: EFE4C76D-4219-43DA-B1F6-4A58ED763686
ms.date: 08/03/2022
ms.keywords: HSTRING_UserUnmarshal, HSTRING_UserUnmarshal function [Windows Runtime], remotesystemadditionalinfo/HSTRING_UserUnmarshal, winrt.hstring_userunmarshal
req.header: winstring.h
req.include-header: Winstring.h, Inspectable.h
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
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HSTRING_UserUnmarshal
 - winstring/HSTRING_UserUnmarshal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-String-l1-1-0.dll
 - API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
 - HSTRING_UserUnmarshal
---

## -description

Unmarshals an [**HSTRING**](/windows/win32/winrt/hstring) object from the RPC buffer.

## -parameters

### -param pFlags

[in]

The data used by RPC.

### -param pBuffer

[in]

The current buffer. This pointer may or may not be aligned on entry.

### -param ppidl

[out]

The string.

## -returns

The value obtained from the returned <b>HRESULT</b> value is one of the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for this function to perform.

</td>
</tr>
</table>

## -see-also

[**HSTRING**](/windows/win32/winrt/hstring)

