---
UID: NC:dxmini.PDX_FLIPVIDEOPORT
title: PDX_FLIPVIDEOPORT
author: windows-sdk-content
description: The DxFlipVideoPort callback function is called when a client of the video miniport driver wants to flip the video port extensions (VPE) object or when autoflipping is enabled.
old-location: display\dxflipvideoport.htm
tech.root: display
ms.assetid: d6047c90-1163-475a-a55b-95ccb0570e3e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DxFlipVideoPort, DxFlipVideoPort callback function [Display Devices], PDX_FLIPVIDEOPORT, PDX_FLIPVIDEOPORT callback, VideoMiniPort_DxApiFunctions_ae9b2d92-5f47-4897-af4e-d8f7cb0f8b39.xml, display.dxflipvideoport, dxmini/DxFlipVideoPort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Desktop
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
 - UserDefined
api_location:
 - dxmini.h
api_name:
 - DxFlipVideoPort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDX_FLIPVIDEOPORT callback function


## -description


The<i> DxFlipVideoPort</i> callback function is called when a client of the video miniport driver wants to flip the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object or when autoflipping is enabled. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - FlipVideoPortInfo

Points to the <a href="https://msdn.microsoft.com/9cf87d19-2db6-48f8-96a6-2b6ac969c774">DDFLIPVIDEOPORTINFO</a> structure that contains the flip information for the surface and VPE object.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpOutput

Reserved for system use.


## -returns



<i>DxFlipVideoPort</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <b>dwFlipVPFlags</b> member of the DDFLIPVIDEOPORTINFO structure at <i>FlipVideoPortInfo</i> uses the DDVPFLIP_VIDEO or DDVPFLIP_VBI flag to indicate whether the surfaces represent VBI surfaces or regular surfaces.




## -see-also




<a href="https://msdn.microsoft.com/9cf87d19-2db6-48f8-96a6-2b6ac969c774">DDFLIPVIDEOPORTINFO</a>
 

 

