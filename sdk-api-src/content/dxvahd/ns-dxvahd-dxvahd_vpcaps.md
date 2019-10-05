---
UID: NS:dxvahd._DXVAHD_VPCAPS
title: DXVAHD_VPCAPS (dxvahd.h)
author: windows-sdk-content
description: Specifies the capabilities of the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\dxvahd_vpcaps.htm
tech.root: medfound
ms.assetid: 25ec6802-ca6e-42d4-b1d5-de7597e3d042
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXVAHD_VPCAPS, DXVAHD_VPCAPS structure [Media Foundation], dxvahd/DXVAHD_VPCAPS, mf.dxvahd_vpcaps
ms.topic: struct
f1_keywords:
- dxvahd/DXVAHD_VPCAPS
dev_langs:
 - c++
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- HeaderDef
api_location:
- dxvahd.h
api_name:
- DXVAHD_VPCAPS
targetos: Windows
req.typenames: DXVAHD_VPCAPS
req.redist: 
ms.custom: 19H1
---

# DXVAHD_VPCAPS structure


## -description


Specifies the capabilities of the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -struct-fields




### -field VPGuid

A GUID that identifies the video processor. This GUID is defined by the device, and is used in various <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device">IDXVAHD_Device</a> methods to specify the video processor.


### -field PastFrames

The number of past reference frames required to perform the optimal video processing.


### -field FutureFrames

The number of future reference frames required to perform the optimal video processing.


### -field ProcessorCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_processor_caps">DXVAHD_PROCESSOR_CAPS</a> enumeration.


### -field ITelecineCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_itelecine_caps">DXVAHD_ITELECINE_CAPS</a> enumeration.


### -field CustomRateCount

The number of custom output frame rates. To get the list of custom frame rates, call the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcustomrates">IDXVAHD_Device::GetVideoProcessorCustomRates</a> method. Custom frame rates are used for frame-rate conversion and inverse telecine.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcaps">IDXVAHD_Device::GetVideoProcessorCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
 

 

