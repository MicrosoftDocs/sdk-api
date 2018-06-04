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

# tagLOCALESIGNATURE structure


## -description



Contains extended font signature information, including two code page bitfields (CPBs) that define the default and supported character sets and code pages. This structure is typically used to represent the relationships between font coverage and locales.




## -struct-fields




### -field lsUsb

A 128-bit Unicode subset bitfield (USB) identifying up to 122 Unicode subranges. Each bit, except the five most significant bits, represents a single subrange. The most significant bit is always 1; the second most significant is reserved and must be 0. Unicode subsets are numbered in accordance with the <a href="https://msdn.microsoft.com/0d67481a-79ff-448c-b77c-a55bf935a22a">OpenType font specification</a>. For a list of possible bitfield values, see <a href="https://msdn.microsoft.com/f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d">Unicode Subset Bitfields</a>.


### -field lsCsbDefault

A code page bitfield that indicates the default OEM and ANSI code pages for a locale. The code pages can be identified by separate bits or a single bit representing a common ANSI and OEM code page. For a list of possible bitfield values, see <a href="https://msdn.microsoft.com/830b1a88-cb0c-4719-b857-4cc2cd67dd5d">Code Page Bitfields</a>.


### -field lsCsbSupported

A code page bitfield that indicates all the code pages in which the locale can be supported. For a list of possible bitfield values, see <a href="https://msdn.microsoft.com/830b1a88-cb0c-4719-b857-4cc2cd67dd5d">Code Page Bitfields</a>.


## -see-also




<a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a>



<a href="https://msdn.microsoft.com/0c8120dd-3270-4343-8b0c-b91ff555f276">Unicode and Character Set Structures</a>
 

 

