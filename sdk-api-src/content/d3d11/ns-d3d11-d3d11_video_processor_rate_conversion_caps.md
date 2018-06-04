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

# D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS structure


## -description


Defines a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.


## -struct-fields




### -field PastFrames

The number of past reference frames required to perform the optimal video processing.




### -field FutureFrames

The number of future reference frames required to perform the optimal video processing.




### -field ProcessorCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/9AD4ED7B-B12E-4DFD-BB85-BC19FC6C755A">D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS</a> enumeration.




### -field ITelecineCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/EE92F877-1B27-4A95-8BB7-01852253D112">D3D11_VIDEO_PROCESSOR_ITELECINE_CAPS</a> enumeration.




### -field CustomRateCount

The number of custom frame rates that the driver supports. To get the list of custom frame rates, call the <a href="https://msdn.microsoft.com/0FA868E6-B0FB-433B-A183-72DDE39B207E">ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate</a> method.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

