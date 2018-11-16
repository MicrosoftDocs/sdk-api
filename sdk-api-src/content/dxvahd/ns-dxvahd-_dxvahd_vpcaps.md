---
UID: NS:dxvahd._DXVAHD_VPCAPS
title: "_DXVAHD_VPCAPS"
author: windows-sdk-content
description: Specifies the capabilities of the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\dxvahd_vpcaps.htm
tech.root: medfound
ms.assetid: 25ec6802-ca6e-42d4-b1d5-de7597e3d042
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DXVAHD_VPCAPS, DXVAHD_VPCAPS structure [Media Foundation], _DXVAHD_VPCAPS, dxvahd/DXVAHD_VPCAPS, mf.dxvahd_vpcaps
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: DXVAHD_VPCAPS
req.redist: 
---

# _DXVAHD_VPCAPS structure


## -description


Specifies the capabilities of the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -struct-fields




### -field VPGuid

A GUID that identifies the video processor. This GUID is defined by the device, and is used in various <a href="https://msdn.microsoft.com/3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd">IDXVAHD_Device</a> methods to specify the video processor.


### -field PastFrames

The number of past reference frames required to perform the optimal video processing.


### -field FutureFrames

The number of future reference frames required to perform the optimal video processing.


### -field ProcessorCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/6fe6b1fe-4eef-427a-b28f-a359b066e552">DXVAHD_PROCESSOR_CAPS</a> enumeration.


### -field ITelecineCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/bf3e0d24-2671-4e79-9cfe-d776d8e5fb47">DXVAHD_ITELECINE_CAPS</a> enumeration.


### -field CustomRateCount

The number of custom output frame rates. To get the list of custom frame rates, call the <a href="https://msdn.microsoft.com/63e835bb-dda2-4449-8474-219a373da82d">IDXVAHD_Device::GetVideoProcessorCustomRates</a> method. Custom frame rates are used for frame-rate conversion and inverse telecine.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/d9423b3f-4a4b-49f0-8018-c19a7b663300">IDXVAHD_Device::GetVideoProcessorCaps</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

