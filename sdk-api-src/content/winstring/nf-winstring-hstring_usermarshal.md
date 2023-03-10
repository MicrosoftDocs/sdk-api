---
UID: NF:winstring.HSTRING_UserMarshal
title: HSTRING_UserMarshal function (winstring.h)
description: The HSTRING_UserMarshal function (winstring.h) marshals an HSTRING object into the RPC buffer. 
helpviewer_keywords: ["HSTRING_UserMarshal","HSTRING_UserMarshal function [Windows Runtime]","remotesystemadditionalinfo/HSTRING_UserMarshal","winrt.hstring_usermarshal"]
old-location: winrt\hstring_usermarshal.htm
tech.root: WinRT
ms.assetid: 986942D6-A1CD-4BED-9AD3-82FB4892E28E
ms.date: 08/03/2022
ms.keywords: HSTRING_UserMarshal, HSTRING_UserMarshal function [Windows Runtime], remotesystemadditionalinfo/HSTRING_UserMarshal, winrt.hstring_usermarshal
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
 - HSTRING_UserMarshal
 - winstring/HSTRING_UserMarshal
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
 - HSTRING_UserMarshal
---

## -description

Marshals an [**HSTRING**](/windows/win32/winrt/hstring) object into the RPC buffer.

## -parameters

### -param pFlags

[in]

The data used by RPC.

### -param pBuffer

[in, out]

The current buffer. This pointer may or may not be aligned on entry.

### -param ppidl

[in]

The string.

## -returns

The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.

## -see-also

[**HSTRING**](/windows/win32/winrt/hstring)

