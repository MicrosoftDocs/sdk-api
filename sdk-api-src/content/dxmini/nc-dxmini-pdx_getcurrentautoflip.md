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

# PDX_GETCURRENTAUTOFLIP callback function


## -description


The<i> DxGetCurrentAutoflip</i> callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface is receiving the current field of video data for capture purposes. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetCurrentAutoflipInInfo

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549393">DDGETCURRENTAUTOFLIPININFO</a> structure that contains the VPE object information.


#### - GetCurrentAutoflipOutInfo

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549396">DDGETCURRENTAUTOFLIPOUTINFO</a> structure that contains the surface information.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


## -returns



<i>DxGetCurrentAutoflip</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <i>DxGetCurrentAutoflip</i> function returns the current index in the autoflip chain of the current surface in the <b>dwSurfaceIndex</b> member of the DDGETCURRENTAUTOFLIPOUTINFO structure at <i>GetCurrentAutoflipOutInfo</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549393">DDGETCURRENTAUTOFLIPININFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549396">DDGETCURRENTAUTOFLIPOUTINFO</a>
 

 

