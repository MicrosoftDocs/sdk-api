---
UID: NF:inspectable.HSTRING_UserUnmarshal64
title: HSTRING_UserUnmarshal64 function (inspectable.h)
description: The HSTRING_UserUnmarshal64 function (inspectable.h) unmarshals an HSTRING object from the RPC buffer.
helpviewer_keywords: ["HSTRING_UserUnmarshal64","HSTRING_UserUnmarshal64 function [Windows Runtime]","remotesystemadditionalinfo/HSTRING_UserUnmarshal64","winrt.hstring_userunmarshal64"]
old-location: winrt\hstring_userunmarshal64.htm
tech.root: WinRT
ms.assetid: CD6F7DCD-23D8-4485-9803-142EE9730458
ms.date: 08/03/2022
ms.keywords: HSTRING_UserUnmarshal64, HSTRING_UserUnmarshal64 function [Windows Runtime], remotesystemadditionalinfo/HSTRING_UserUnmarshal64, winrt.hstring_userunmarshal64
req.header: inspectable.h
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
 - HSTRING_UserUnmarshal64
 - inspectable/HSTRING_UserUnmarshal64
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
 - HSTRING_UserUnmarshal64
---

# HSTRING_UserUnmarshal64 function


## -description

Unmarshals an <a href="/windows/desktop/WinRT/hstring">HSTRING</a> object from the RPC buffer.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in]

The current buffer. This pointer may or may not be aligned on entry.

### -param unnamedParam3 [out]

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

<a href="/windows/desktop/WinRT/hstring">HSTRING</a>
