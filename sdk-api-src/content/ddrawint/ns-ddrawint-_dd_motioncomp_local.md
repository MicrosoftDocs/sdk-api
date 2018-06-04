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

# _DD_MOTIONCOMP_LOCAL structure


## -description


The DD_MOTIONCOMP_LOCAL structure contains local data for each individual Microsoft DirectDraw motion compensation object. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current DirectDraw process only.


### -field guid

Specifies a GUID that describes the motion compensation process being used.


### -field dwUncompWidth

Indicates the width in pixels of the uncompressed output frame. 


### -field dwUncompHeight

Indicates the height in pixels of the uncompressed output frame. 


### -field ddUncompPixelFormat

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure that contains the pixel format of the uncompressed output frame. 


### -field dwDriverReserved1


### -field dwDriverReserved2


### -field dwDriverReserved3

Are reserved for use by the display driver. 


### -field lpDriverReserved1


### -field lpDriverReserved2


### -field lpDriverReserved3

Are reserved for use by the display driver. 

