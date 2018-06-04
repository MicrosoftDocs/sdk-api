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

# tagEMRTEXT structure


## -description



The <b>EMRTEXT</b> structure contains members for text output.




## -struct-fields




### -field ptlReference

The logical coordinates of the reference point used to position the string.


### -field nChars

The number of characters in the string.


### -field offString

The offset to the string.


### -field fOptions

A value that indicates how to use the application-defined rectangle. This member can be a combination of the ETO_CLIPPED and ETO_OPAQUE values.


### -field rcl

An optional clipping and/or opaquing rectangle, in logical units.


### -field offDx

The offset to the intercharacter spacing array.


## -remarks



The <b>EMRTEXT</b> structure is used as a member in the <a href="https://msdn.microsoft.com/1d9b0b32-6a51-481a-9589-3de832d746d7">EMREXTTEXTOUT</a> and <a href="https://msdn.microsoft.com/9c1decdd-fe6f-4220-abba-7547ab5427ba">EMRPOLYTEXTOUT</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>
 

 

