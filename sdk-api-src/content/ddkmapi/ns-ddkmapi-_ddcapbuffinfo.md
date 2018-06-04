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

# _DDCAPBUFFINFO structure


## -description


The DDCAPBUFFINFO structure contains the capture information. 


## -struct-fields




### -field dwFieldNumber

Indicates the internal field number of the field captured.


### -field bPolarity

Specifies whether the captured field is an even or odd field. A value of 0x00000001 indicates even, 0x00000000 indicates odd.


### -field liTimeStamp

Used by Microsoft DirectDraw and should be ignored by the driver.


### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550599">DD_DXAPI_ADDVPCAPTUREBUFFER</a> operation. Contains DD_OK if the capture buffer contains valid data.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549199">DDADDVPCAPTUREBUFF</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550599">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

