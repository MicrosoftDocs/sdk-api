---
UID: NS:hstring.HSTRING_HEADER
title: HSTRING_HEADER
author: windows-driver-content
description: Represents a header for an HSTRING.
old-location: winrt\hstring_header.htm
old-project: WinRT
ms.assetid: E63E73A7-1908-4CEC-ADCB-1A3D23BE8A3B
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: HSTRING_HEADER, HSTRING_HEADER structure [Windows Runtime], hstring/HSTRING_HEADER, winrt.hstring_header
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: HSTRING_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	hstring.h
api_name:
-	HSTRING_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HSTRING_HEADER structure


## -description


Represents a header for an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>.


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




<a href="https://msdn.microsoft.com/0361BB7E-DA49-4289-A93E-DE7AAB8712AC">WindowsCreateStringReference</a>
 

 

