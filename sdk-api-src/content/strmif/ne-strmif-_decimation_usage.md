---
UID: NE:strmif._DECIMATION_USAGE
title: "_DECIMATION_USAGE"
author: windows-sdk-content
description: Describes the strategy that the Overlay Mixer Filter filter uses to scale the video image down to a smaller size.
old-location: dshow\decimation_usage.htm
old-project: DirectShow
ms.assetid: 4c39f7f9-2d9c-4db5-9a2b-cf221ddedf80
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DECIMATION_DEFAULT, DECIMATION_LEGACY, DECIMATION_USAGE, DECIMATION_USAGE , DECIMATION_USAGE enumeration [DirectShow], DECIMATION_USAGEEnumeration, DECIMATION_USE_DECODER_ONLY, DECIMATION_USE_OVERLAY_ONLY, DECIMATION_USE_VIDEOPORT_ONLY, _DECIMATION_USAGE, dshow.decimation_usage, strmif/DECIMATION_DEFAULT, strmif/DECIMATION_LEGACY, strmif/DECIMATION_USAGE, strmif/DECIMATION_USE_DECODER_ONLY, strmif/DECIMATION_USE_OVERLAY_ONLY, strmif/DECIMATION_USE_VIDEOPORT_ONLY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: DECIMATION_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DECIMATION_USAGE
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# _DECIMATION_USAGE enumeration


## -description



Describes the strategy that the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer Filter</a> filter uses to scale the video image down to a smaller size.




## -enum-fields




### -field DECIMATION_LEGACY

Decimate the video by taking the following steps, in the order listed, until one of them succeeds.

<ol>
<li>Try to use the overlay scaler on the VGA chip.</li>
<li>If the Overlay Mixer is connected through a video port, try to use the scaler on the video port.</li>
<li>Crop the video image.</li>
</ol>

### -field DECIMATION_USE_DECODER_ONLY

Decimate using the scaler on the video decoder. If that fails, crop the video image.


### -field DECIMATION_USE_VIDEOPORT_ONLY

Decimate using the scaler on the video port. If that fails, crop the video image.


### -field DECIMATION_USE_OVERLAY_ONLY

Decimate using the overlay scaler on the VGA chip. If that fails, crop the video image.


### -field DECIMATION_DEFAULT

Decimate the video by taking the following steps, in the order listed, until one of them succeeds.

<ol>
<li>Try to use the scaler on the video decoder.</li>
<li>Try to use the overlay scaler on the VGA chip.</li>
<li>If the Overlay Mixer is connected through a video port, try to use the scaler on the video port.</li>
<li>Crop the video image.</li>
</ol>
This mode is the default decimation strategy.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/fd435eff-a4bc-40b3-8aa7-50d78d17e4ce">IAMVideoDecimationProperties</a>
 

 

