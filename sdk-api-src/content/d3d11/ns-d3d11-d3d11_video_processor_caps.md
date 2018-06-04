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

# D3D11_VIDEO_PROCESSOR_CAPS structure


## -description


Describes the capabilities of a Microsoft Direct3D 11 video processor.


## -struct-fields




### -field DeviceCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/35335C16-D8BD-4C52-9C9A-4B28DCB53A7F">D3D11_VIDEO_PROCESSOR_DEVICE_CAPS</a>  enumeration.


### -field FeatureCaps

A bitwise <b>OR</b> of zero or more flags from the   <a href="https://msdn.microsoft.com/A40E33D4-E8F3-4348-9135-DD56BABBFA85">D3D11_VIDEO_PROCESSOR_FEATURE_CAPS</a> enumeration.


### -field FilterCaps

A bitwise <b>OR</b> of zero or more flags from the  <a href="mf.d3d11_video_processpr_filter_caps">D3D11_VIDEO_PROCESSPR_FILTER_CAPS</a> enumeration.


### -field InputFormatCaps

A bitwise <b>OR</b> of zero or more flags from the  <a href="https://msdn.microsoft.com/E14D25B7-9F97-465A-ADA5-820BB2952E00">D3D11_VIDEO_PROCESSOR_FORMAT_CAPS</a> enumeration.


### -field AutoStreamCaps

A bitwise <b>OR</b> of zero or more flags from the  <a href="https://msdn.microsoft.com/73836F8D-0A0C-4719-A27F-AC13617380D2">D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS</a> enumeration.


### -field StereoCaps

A bitwise <b>OR</b> of zero or more flags from the   <a href="https://msdn.microsoft.com/352B982A-E950-4593-973E-ECDAFCF2A5F4">D3D11_VIDEO_PROCESSOR_STEREO_CAPS</a> enumeration.


### -field RateConversionCapsCount

The number of frame-rate conversion capabilities. To enumerate the frame-rate conversion capabilities, call the <a href="https://msdn.microsoft.com/2DB74CB9-C6B3-477A-9EF9-6E2EC1DE37D6">ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps</a> method.


### -field MaxInputStreams

The maximum number of input streams that can be enabled at the same time.




### -field MaxStreamStates

The maximum number of input streams for which the device can store state data.


## -remarks



The video processor stores state information for each input stream. These states persist between blits. With each blit, the application selects which streams to enable or disable. Disabling a stream does not affect the state information for that stream.

The <b>MaxStreamStates</b> member gives the maximum number of stream states that can be saved. The <b>MaxInputStreams</b> member gives the maximum number of streams that can be enabled during a blit. These two values can differ.






## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>
 

 

