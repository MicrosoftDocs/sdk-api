---
UID: NC:dxmini.PDX_GETCURRENTAUTOFLIP
title: PDX_GETCURRENTAUTOFLIP (dxmini.h)
description: The DxGetCurrentAutoflip callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface is receiving the current field of video data for capture purposes.
helpviewer_keywords: ["DxGetCurrentAutoflip","DxGetCurrentAutoflip callback function [Display Devices]","PDX_GETCURRENTAUTOFLIP","PDX_GETCURRENTAUTOFLIP callback","VideoMiniPort_DxApiFunctions_1e8f1780-efe2-4f65-955b-887dc9a11358.xml","display.dxgetcurrentautoflip","dxmini/DxGetCurrentAutoflip"]
old-location: display\dxgetcurrentautoflip.htm
tech.root: display
ms.assetid: 25010ffb-893f-401f-8883-f5a08e7014bf
ms.date: 12/05/2018
ms.keywords: DxGetCurrentAutoflip, DxGetCurrentAutoflip callback function [Display Devices], PDX_GETCURRENTAUTOFLIP, PDX_GETCURRENTAUTOFLIP callback, VideoMiniPort_DxApiFunctions_1e8f1780-efe2-4f65-955b-887dc9a11358.xml, display.dxgetcurrentautoflip, dxmini/DxGetCurrentAutoflip
f1_keywords:
- dxmini/DxGetCurrentAutoflip
dev_langs:
- c++
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
- DxGetCurrentAutoflip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDX_GETCURRENTAUTOFLIP callback function


## -description


The<i> DxGetCurrentAutoflip</i> callback function is called when the device is hardware autoflipping and a client of the video miniport driver wants to know which surface is receiving the current field of video data for capture purposes. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetCurrentAutoflipInInfo

Points to the <a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddgetcurrentautoflipininfo">DDGETCURRENTAUTOFLIPININFO</a> structure that contains the VPE object information.


#### - GetCurrentAutoflipOutInfo

Points to the <a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddgetcurrentautoflipoutinfo">DDGETCURRENTAUTOFLIPOUTINFO</a> structure that contains the surface information.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


## -returns



<i>DxGetCurrentAutoflip</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <i>DxGetCurrentAutoflip</i> function returns the current index in the autoflip chain of the current surface in the <b>dwSurfaceIndex</b> member of the DDGETCURRENTAUTOFLIPOUTINFO structure at <i>GetCurrentAutoflipOutInfo</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddgetcurrentautoflipininfo">DDGETCURRENTAUTOFLIPININFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddgetcurrentautoflipoutinfo">DDGETCURRENTAUTOFLIPOUTINFO</a>
 

 

