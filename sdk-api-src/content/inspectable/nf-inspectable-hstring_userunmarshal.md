---
UID: NF:inspectable.HSTRING_UserUnmarshal
title: HSTRING_UserUnmarshal function (inspectable.h)
description: Unmarshals an HSTRING object from the RPC buffer.
helpviewer_keywords: ["HSTRING_UserUnmarshal","HSTRING_UserUnmarshal function [Windows Runtime]","remotesystemadditionalinfo/HSTRING_UserUnmarshal","winrt.hstring_userunmarshal"]
old-location: winrt\hstring_userunmarshal.htm
tech.root: WinRT
ms.assetid: EFE4C76D-4219-43DA-B1F6-4A58ED763686
ms.date: 12/05/2018
ms.keywords: HSTRING_UserUnmarshal, HSTRING_UserUnmarshal function [Windows Runtime], remotesystemadditionalinfo/HSTRING_UserUnmarshal, winrt.hstring_userunmarshal
f1_keywords:
- inspectable/HSTRING_UserUnmarshal
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HSTRING_UserUnmarshal function


## -description


Unmarshals an <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a> object from the RPC buffer.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD




#### - pBuffer [in]

The current buffer. This pointer may or may not be aligned on entry.


#### - pFlags [in]

The data used by RPC.


#### - ppidl [out]

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




<a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>
 

 

