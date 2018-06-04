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

# PDX_FLIPVIDEOPORT callback function


## -description


The<i> DxFlipVideoPort</i> callback function is called when a client of the video miniport driver wants to flip the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object or when autoflipping is enabled. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - FlipVideoPortInfo

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549347">DDFLIPVIDEOPORTINFO</a> structure that contains the flip information for the surface and VPE object.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpOutput

Reserved for system use.


## -returns



<i>DxFlipVideoPort</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <b>dwFlipVPFlags</b> member of the DDFLIPVIDEOPORTINFO structure at <i>FlipVideoPortInfo</i> uses the DDVPFLIP_VIDEO or DDVPFLIP_VBI flag to indicate whether the surfaces represent VBI surfaces or regular surfaces.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549347">DDFLIPVIDEOPORTINFO</a>
 

 

