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
 

 

