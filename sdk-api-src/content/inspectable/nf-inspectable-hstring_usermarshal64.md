---
UID: NF:inspectable.HSTRING_UserMarshal64
title: HSTRING_UserMarshal64 function (inspectable.h)
description: Marshals an HSTRING object into the RPC buffer.
helpviewer_keywords: ["HSTRING_UserMarshal64","HSTRING_UserMarshal64 function [Windows Runtime]","remotesystemadditionalinfo/HSTRING_UserMarshal64","winrt.hstring_usermarshal64"]
old-location: winrt\hstring_usermarshal64.htm
tech.root: WinRT
ms.assetid: 31B9885A-FE5B-4375-883E-F8DBD5F2F4D1
ms.date: 12/05/2018
ms.keywords: HSTRING_UserMarshal64, HSTRING_UserMarshal64 function [Windows Runtime], remotesystemadditionalinfo/HSTRING_UserMarshal64, winrt.hstring_usermarshal64
f1_keywords:
- inspectable/HSTRING_UserMarshal64
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
- HSTRING_UserMarshal64
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HSTRING_UserMarshal64 function


## -description


Marshals an <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a> object into the RPC buffer.


## -parameters




### -param arg1 [in]

The data used by RPC.


### -param arg2 [in, out]

The current buffer. This pointer may or may not be aligned on entry.


### -param arg3 [in]

The string.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>
 

 

