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

# _VMRVIDEOSTREAMINFO structure


## -description



This topic applies to Windows XP or later.
          

The <code>VMRVIDEOSTREAMINFO</code> structure is used in the VMR-7 filter's call to <a href="https://msdn.microsoft.com/5af73543-d391-404a-9797-8fbb3f24879c">IVMRImageCompositor::CompositeImage</a> on the image compositor.




## -struct-fields




### -field pddsVideoSurface

Specifies the DirectDraw surface that contains the video to be composited.


### -field dwWidth

Specifies the width of the video rectangle.


### -field dwHeight

Specifies the height of the video rectangle.


### -field dwStrmID

Specifies the input stream. This value corresponds to the input pin.


### -field fAlpha

Specifies the alpha value for this stream. (Not per-pixel alpha.)


### -field ddClrKey

Specifies the source color key value or -1 if color keying is not to be used for this stream.


### -field rNormal

Specifies the position of the image in composition space.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

