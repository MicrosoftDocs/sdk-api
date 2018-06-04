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

# _DDSETSTATEININFO structure


## -description


The DDSETSTATEININFO structure contains the surface and <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object information. 


## -struct-fields




### -field lpSurfaceData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550335">DDSURFACEDATA</a> structure that contains the surface information. 


### -field lpVideoPortData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550395">DDVIDEOPORTDATA</a> structure that contains the VPE object information.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550335">DDSURFACEDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550395">DDVIDEOPORTDATA</a>



<a href="https://msdn.microsoft.com/f2d7f248-017e-4375-b0a0-49de65192511">DxSetState</a>
 

 

