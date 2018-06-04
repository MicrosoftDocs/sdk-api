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

# _DD_VIDEOPORT_LOCAL structure


## -description


The DD_VIDEOPORT_LOCAL structure contains <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a>-related data that is unique to an individual Microsoft DirectDraw VPE object.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current DirectDraw process only.


### -field ddvpDesc

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550402">DDVIDEOPORTDESC</a> structure that describes the VPE object.


### -field ddvpInfo

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550447">DDVIDEOPORTINFO</a> structure that describes the transfer of video data to a surface.


### -field lpSurface

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551730">DD_SURFACE_INT</a> structure for the surface receiving the video data.


### -field lpVBISurface

Points to a DD_SURFACE_INT structure for the surface receiving the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> data.


### -field dwNumAutoflip

Specifies the number of current autoflip surfaces.


### -field dwNumVBIAutoflip

Specifies the number of VBI surfaces currently being autoflipped.


### -field dwReserved1

Reserved for use by the display driver.


### -field dwReserved2

Reserved for use by the display driver.


### -field dwReserved3

Reserved for use by the display driver.


## -remarks



This structure is initialized and filled in by DirectDraw. Except for the <b>dwReserved1</b>, <b>dwReserved2</b>, and <b>dwReserved3</b> members, the driver must not modify any other members of the DD_VIDEOPORT_LOCAL structure.



