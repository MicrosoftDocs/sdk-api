---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagFONTSIGNATURE structure


## -description



Contains information identifying the code pages and Unicode subranges for which a given font provides glyphs.




## -struct-fields




### -field fsUsb

A 128-bit Unicode subset bitfield (USB) identifying up to 126 Unicode subranges. Each bit, except the two most significant bits, represents a single subrange. The most significant bit is always 1 and identifies the bitfield as a font signature; the second most significant bit is reserved and must be 0. Unicode subranges are numbered in accordance with the ISO 10646 standard. For more information, see <a href="https://msdn.microsoft.com/f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d">Unicode Subset Bitfields</a>.


### -field fsCsb

A 64-bit, code-page bitfield (CPB) that identifies a specific character set or code page. Code pages are in the lower 32 bits of this bitfield. The high 32 are used for non-Windows code pages. For more information, see <a href="https://msdn.microsoft.com/830b1a88-cb0c-4719-b857-4cc2cd67dd5d">Code Page Bitfields</a>.


## -remarks



GDI relies on Windows code pages fitting within a 32-bit value. Furthermore, the highest 2 bits within this value are reserved for GDI internal use and may not be assigned to code pages.




## -see-also




<a href="https://msdn.microsoft.com/54510d73-f2a2-4176-8080-cdf855e99217">LOCALESIGNATURE</a>



<a href="https://msdn.microsoft.com/0c8120dd-3270-4343-8b0c-b91ff555f276">Unicode and Character Set Structures</a>
 

 

