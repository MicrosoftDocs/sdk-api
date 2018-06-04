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

# _DDVIDEOPORTDESC structure


## -description


The DDVIDEOPORTDESC structure describes the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object being created.


## -struct-fields




### -field dwSize

Specifies the size in bytes of the DDVIDEOPORTDESC structure.


### -field dwFieldWidth

Specifies the width in pixels of the incoming video stream.


### -field dwVBIWidth

Specifies the width, in number of samples, of the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> data in the incoming video stream.


### -field dwFieldHeight

Specifies the field height in scan lines of the incoming video stream.


### -field dwMicrosecondsPerField

Specifies the time interval in microseconds between live video VSYNCs. This number should be rounded up to the nearest whole microsecond.


### -field dwMaxPixelsPerSecond

Specifies the maximum pixel rate per second.


### -field dwVideoPortID

Specifies the ID of the hardware video port to be used. This ID should range from 0 to (<b>dwMaxVideoPorts</b> -1), where <b>dwMaxVideoPorts</b> is a member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a> structure.


### -field dwReserved1

Reserved for system use and should be ignored by the driver. 


### -field VideoPortType

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550388">DDVIDEOPORTCONNECT</a> structure describing the connection characteristics of the hardware video port.


### -field dwReserved2

Reserved for future use and should be ignored by the driver.


### -field dwReserved3

Reserved for future use and should be ignored by the driver.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550388">DDVIDEOPORTCONNECT</a>
 

 

