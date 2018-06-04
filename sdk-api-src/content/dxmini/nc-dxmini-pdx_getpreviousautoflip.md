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

# PDX_GETPREVIOUSAUTOFLIP callback function


## -description


The<i> DxGetPreviousAutoflip</i> callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface received the previous field of video data for capture purposes. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetPreviousAutoflipInInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549485">DDGETPREVIOUSAUTOFLIPININFO</a> structure that contains the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object information.


#### - GetPreviousAutoflipOutInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549489">DDGETPREVIOUSAUTOFLIPOUTINFO</a> structure that contains the index of the autoflip chain.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


## -returns



<i>DxGetPreviousAutoflip</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



If interleaving, the surface that received the previous field may be the same surface that is receiving the current field. 

<i>DxGetPreviousAutoflip</i> returns the index in the autoflip chain of the correct surface in the <b>dwSurfaceIndex</b> member of the DDGETPREVIOUSAUTOFLIPOUTINFO structure at <i>GetPreviousAutoflipOutInfo</i>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549485">DDGETPREVIOUSAUTOFLIPININFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549489">DDGETPREVIOUSAUTOFLIPOUTINFO</a>
 

 

