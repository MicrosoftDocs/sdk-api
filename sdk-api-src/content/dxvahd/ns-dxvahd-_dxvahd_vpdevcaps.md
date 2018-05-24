---
UID: NS:dxvahd._DXVAHD_VPDEVCAPS
title: "_DXVAHD_VPDEVCAPS"
author: windows-driver-content
description: Specifies the capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\dxvahd_vpdevcaps.htm
old-project: medfound
ms.assetid: 340669d4-2a84-4030-83c3-a61469fdfd61
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DXVAHD_VPDEVCAPS, DXVAHD_VPDEVCAPS structure [Media Foundation], _DXVAHD_VPDEVCAPS, dxvahd/DXVAHD_VPDEVCAPS, mf.dxvahd_vpdevcaps
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
req.typenames: DXVAHD_VPDEVCAPS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxvahd.h
api_name:
-	DXVAHD_VPDEVCAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_VPDEVCAPS structure


## -description


Specifies the capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -struct-fields




### -field DeviceType

Specifies the device type, as a member of the <a href="https://msdn.microsoft.com/c472f2c6-214d-4bb0-ba9d-8dd04ff2a646">DXVAHD_DEVICE_TYPE</a> enumeration.


### -field DeviceCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/1f3dde4c-cd9d-4361-b2b2-db3c9d2ea146">DXVAHD_DEVICE_CAPS</a> enumeration.


### -field FeatureCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/6014780b-3b8a-48d6-ae30-b48127a2c274">DXVAHD_FEATURE_CAPS</a> enumeration.


### -field FilterCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/2f4e0b48-fbce-49e8-9ea8-1b6f0a022d60">DXVAHD_FILTER_CAPS</a> enumeration.


### -field InputFormatCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/ddfff29c-3a40-4238-93e7-821c4ffc27af">DXVAHD_INPUT_FORMAT_CAPS</a> enumeration.


### -field InputPool

The memory pool that is required for the input video surfaces.


### -field OutputFormatCount

The number of supported output formats. To get the list of output formats, call the <a href="https://msdn.microsoft.com/e701014d-c112-42fa-9bf5-88cb31424006">IDXVAHD_Device::GetVideoProcessorOutputFormats</a> method.


### -field InputFormatCount

The number of supported input formats. To get the list of input formats, call the <a href="https://msdn.microsoft.com/b660d111-7bd1-4345-b229-1825d830bab4">IDXVAHD_Device::GetVideoProcessorInputFormats</a> method.


### -field VideoProcessorCount

The number of video processors. Each video processor represents a  distinct set of processing capabilities. To get the capabilities of each video processor, call the <a href="https://msdn.microsoft.com/d9423b3f-4a4b-49f0-8018-c19a7b663300">IDXVAHD_Device::GetVideoProcessorCaps</a> method. To create a video processor, call the <a href="https://msdn.microsoft.com/903e2c05-e4d4-42ca-a28d-6d4738ae6cfc">IDXVAHD_Device::CreateVideoProcessor</a> method. 


### -field MaxInputStreams

The maximum number of input streams that can be enabled at the same time.


### -field MaxStreamStates

The maximum number of input streams for which the device can store state data. 


## -remarks



In DXVA-HD, the device stores state information for each input stream. These states persist between blits. With each blit, the application selects which streams to enable or disable. Disabling a stream does not affect the state information for that stream.



The <b>MaxStreamStates</b> member gives the maximum number of stream states that can be set by the application. The <b>MaxInputStreams</b> member gives the maximum number of streams that can be enabled during a blit. These two values can differ.

To set the state data for a stream, call <a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

