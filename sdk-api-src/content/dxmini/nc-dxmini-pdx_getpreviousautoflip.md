---
UID: NC:dxmini.PDX_GETPREVIOUSAUTOFLIP
title: PDX_GETPREVIOUSAUTOFLIP
author: windows-sdk-content
description: The DxGetPreviousAutoflip callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface received the previous field of video data for capture purposes.
old-location: display\dxgetpreviousautoflip.htm
tech.root: display
ms.assetid: 3b19e4be-413c-4014-b414-cb2ba3e14b14
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DxGetPreviousAutoflip, DxGetPreviousAutoflip callback function [Display Devices], PDX_GETPREVIOUSAUTOFLIP, PDX_GETPREVIOUSAUTOFLIP callback, VideoMiniPort_DxApiFunctions_07351af6-3fdc-4a60-852f-23ea28bc6e2b.xml, display.dxgetpreviousautoflip, dxmini/DxGetPreviousAutoflip
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
 - DxGetPreviousAutoflip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDX_GETPREVIOUSAUTOFLIP callback function


## -description


The<i> DxGetPreviousAutoflip</i> callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface received the previous field of video data for capture purposes. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetPreviousAutoflipInInfo

Points to a <a href="https://msdn.microsoft.com/44816bbe-9ec2-4f96-a18c-442359aa36ad">DDGETPREVIOUSAUTOFLIPININFO</a> structure that contains the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object information.


#### - GetPreviousAutoflipOutInfo

Points to a <a href="https://msdn.microsoft.com/3009425c-00ba-4be5-be81-65905abf4a2a">DDGETPREVIOUSAUTOFLIPOUTINFO</a> structure that contains the index of the autoflip chain.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


## -returns



<i>DxGetPreviousAutoflip</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



If interleaving, the surface that received the previous field may be the same surface that is receiving the current field. 

<i>DxGetPreviousAutoflip</i> returns the index in the autoflip chain of the correct surface in the <b>dwSurfaceIndex</b> member of the DDGETPREVIOUSAUTOFLIPOUTINFO structure at <i>GetPreviousAutoflipOutInfo</i>. 




## -see-also




<a href="https://msdn.microsoft.com/44816bbe-9ec2-4f96-a18c-442359aa36ad">DDGETPREVIOUSAUTOFLIPININFO</a>



<a href="https://msdn.microsoft.com/3009425c-00ba-4be5-be81-65905abf4a2a">DDGETPREVIOUSAUTOFLIPOUTINFO</a>
 

 

