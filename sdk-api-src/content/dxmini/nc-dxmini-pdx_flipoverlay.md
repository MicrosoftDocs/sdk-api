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

# PDX_FLIPOVERLAY callback function


## -description


The<i> DxFlipOverlay</i> callback function is called when a client of the video miniport driver wants to flip the overlay or when autoflipping is enabled. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - FlipOverlayInfo

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549323">DDFLIPOVERLAYINFO</a> structure that contains the flip information for the surface.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpOutput

Reserved for system use.


## -returns



<i>DxFlipOverlay</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



If a hardware video port is not used and the client still wants the overlay to bob the data, the <b>dwFlags</b> member of the DDFLIPOVERLAYINFO structure at <i>FlipOverlayInfo</i> specifies the polarity of the data in the field being flipped (using the DDFLIP_EVEN or DDFLIP_ODD flags). These flags are not used when flipping a surface that is fed by a hardware video port. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549323">DDFLIPOVERLAYINFO</a>
 

 

