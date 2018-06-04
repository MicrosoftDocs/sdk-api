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

# tagEMRPOLYTEXTOUTA structure


## -description



The <b>EMRPOLYTEXTOUTA</b> and <b>EMRPOLYTEXTOUTW</b> structures contain members for the <b>PolyTextOut</b> enhanced metafile record.




## -struct-fields




### -field emr

Base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field iGraphicsMode

Current graphics mode. This member can be either the GM_COMPATIBLE or GM_ADVANCED value.


### -field exScale

X-scaling factor from page units to .01mm units if the graphics mode is the GM_COMPATIBLE value.


### -field eyScale

Y-scaling factor from page units to .01mm units if the graphics mode is the GM_COMPATIBLE value.


### -field cStrings

Number of strings.


### -field aemrtext

<b>EMRTEXT</b> structure, which is followed by the string and the intercharacter spacing array.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

