---
UID: NF:remotesystemadditionalinfo.HSTRING_UserSize
title: HSTRING_UserSize function (remotesystemadditionalinfo.h)
description: The HSTRING_UserSize function calculates the wire size of the HSTRING object, and retrieves its handle and data. (HSTRING_UserSize)
helpviewer_keywords: ["HSTRING_UserSize","HSTRING_UserSize function [Windows Runtime]","remotesystemadditionalinfo/HSTRING_UserSize","winrt.hstring_usersize"]
old-location: winrt\hstring_usersize.htm
tech.root: WinRT
ms.assetid: F258F308-7A16-4C24-9770-F6D8A1604811
ms.date: 08/03/2022
ms.keywords: HSTRING_UserSize, HSTRING_UserSize function [Windows Runtime], remotesystemadditionalinfo/HSTRING_UserSize, winrt.hstring_usersize
req.header: remotesystemadditionalinfo.h
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
 - HSTRING_UserSize
 - remotesystemadditionalinfo/HSTRING_UserSize
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
 - HSTRING_UserSize
---

# HSTRING_UserSize function


## -description

Calculates the wire size of the <a href="/windows/desktop/WinRT/hstring">HSTRING</a> object, and gets its handle and data.

## -parameters

### -param unnamedParam1

TBD

### -param unnamedParam2

TBD

### -param unnamedParam3

TBD




#### - StartingSize [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the <a href="/windows/desktop/WinRT/hstring">HSTRING</a> object to be properly aligned when it will be marshaled to the buffer.


#### - pFlags [in]

The data used by RPC.


#### - ppidl [in]

The string.

## -returns

The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/WinRT/hstring">HSTRING</a>
