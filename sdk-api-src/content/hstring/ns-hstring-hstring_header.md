---
UID: NS:hstring.HSTRING_HEADER
title: HSTRING_HEADER (hstring.h)
description: Represents a header for an HSTRING.
helpviewer_keywords: ["HSTRING_HEADER","HSTRING_HEADER structure [Windows Runtime]","hstring/HSTRING_HEADER","winrt.hstring_header"]
old-location: winrt\hstring_header.htm
tech.root: WinRT
ms.assetid: E63E73A7-1908-4CEC-ADCB-1A3D23BE8A3B
ms.date: 12/05/2018
ms.keywords: HSTRING_HEADER, HSTRING_HEADER structure [Windows Runtime], hstring/HSTRING_HEADER, winrt.hstring_header
f1_keywords:
- hstring/HSTRING_HEADER
dev_langs:
- c++
req.header: hstring.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- hstring.h
api_name:
- HSTRING_HEADER
targetos: Windows
req.typenames: HSTRING_HEADER
req.redist: 
ms.custom: 19H1
---

# HSTRING_HEADER structure


## -description


Represents a header for an <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>.


## -struct-fields




### -field Reserved


### -field Reserved.Reserved1

<b>Type: <b>PVOID</b>
</b>
Reserved for future use.


### -field Reserved.Reserved2

<b>Type: <b>char[24]</b>
</b>
Reserved for future use in a 64-bit environment.

<b>Type: <b>char[20]</b>
</b>
Reserved for future use in a non 64-bit environment.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowscreatestringreference">WindowsCreateStringReference</a>
 

 

