---
UID: NC:dxmini.PDX_GETCURRENTAUTOFLIP
title: PDX_GETCURRENTAUTOFLIP
author: windows-driver-content
description: The DxGetCurrentAutoflip callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface is receiving the current field of video data for capture purposes.
old-location: display\dxgetcurrentautoflip.htm
old-project: display
ms.assetid: 25010ffb-893f-401f-8883-f5a08e7014bf
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: DxGetCurrentAutoflip, DxGetCurrentAutoflip callback function [Display Devices], PDX_GETCURRENTAUTOFLIP, VideoMiniPort_DxApiFunctions_1e8f1780-efe2-4f65-955b-887dc9a11358.xml, display.dxgetcurrentautoflip, dxmini/DxGetCurrentAutoflip
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
req.typenames: DXGI_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	dxmini.h
api_name:
-	DxGetCurrentAutoflip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# PDX_GETCURRENTAUTOFLIP callback


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
 

 

