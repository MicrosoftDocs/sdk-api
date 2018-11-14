---
UID: NS:dvp._DDVIDEOPORTDESC
title: "_DDVIDEOPORTDESC"
author: windows-sdk-content
description: The DDVIDEOPORTDESC structure describes the video port extensions (VPE) object being created.
old-location: display\ddvideoportdesc.htm
tech.root: display
ms.assetid: efd5907c-ed75-40be-b568-7c305310f79b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPDDVIDEOPORTDESC, DDVIDEOPORTDESC, DDVIDEOPORTDESC structure [Display Devices], _DDVIDEOPORTDESC, ddstrcts_4fab2afd-4b57-49cc-b288-3ff8af49c3ba.xml, display.ddvideoportdesc, dvp/DDVIDEOPORTDESC"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dvp.h
req.include-header: Dvp.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dvp.h
api_name:
 - DDVIDEOPORTDESC
product: Windows
targetos: Windows
req.typenames: "*LPDDVIDEOPORTDESC, DDVIDEOPORTDESC"
req.redist: 
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

Specifies the ID of the hardware video port to be used. This ID should range from 0 to (<b>dwMaxVideoPorts</b> -1), where <b>dwMaxVideoPorts</b> is a member of the <a href="https://msdn.microsoft.com/529d60b5-658d-4d55-a599-fa35386c01a7">DDCORECAPS</a> structure.


### -field dwReserved1

Reserved for system use and should be ignored by the driver. 


### -field VideoPortType

Specifies a <a href="https://msdn.microsoft.com/54c1bb05-37a8-4841-808b-2eb9d1ecd7a3">DDVIDEOPORTCONNECT</a> structure describing the connection characteristics of the hardware video port.


### -field dwReserved2

Reserved for future use and should be ignored by the driver.


### -field dwReserved3

Reserved for future use and should be ignored by the driver.


## -see-also




<a href="https://msdn.microsoft.com/529d60b5-658d-4d55-a599-fa35386c01a7">DDCORECAPS</a>



<a href="https://msdn.microsoft.com/54c1bb05-37a8-4841-808b-2eb9d1ecd7a3">DDVIDEOPORTCONNECT</a>
 

 

