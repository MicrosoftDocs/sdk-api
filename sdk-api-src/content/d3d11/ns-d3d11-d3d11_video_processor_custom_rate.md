---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
title: D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
author: windows-sdk-content
description: Specifies a custom rate for frame-rate conversion or inverse telecine (IVTC).
old-location: mf\d3d11_video_processor_custom_rate.htm
old-project: medfound
ms.assetid: 237357C8-546E-41E5-8002-E5499E39DA72
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_CUSTOM_RATE, D3D11_VIDEO_PROCESSOR_CUSTOM_RATE structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_CUSTOM_RATE, mf.d3d11_video_processor_custom_rate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_PROCESSOR_CUSTOM_RATE structure


## -description


Specifies a custom rate for frame-rate conversion or inverse telecine (IVTC).




## -struct-fields




### -field CustomRate

The ratio of the output frame rate to the input frame rate, expressed as a <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure that holds a rational number.




### -field OutputFrames

The number of output frames that will be generated for every <i>N</i> input samples, where <i>N</i> = <b>InputFramesOrFields</b>.




### -field InputInterlaced

If <b>TRUE</b>, the input stream must be interlaced. Otherwise, the input stream must be progressive.




### -field InputFramesOrFields

The number of input fields or frames for every <i>N</i> output frames that will be generated, where <i>N</i> = <b>OutputFrames</b>.




## -remarks



The <b>CustomRate</b> member gives the rate conversion factor, while the remaining members define the pattern of input and output samples.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/0FA868E6-B0FB-433B-A183-72DDE39B207E">ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate</a>
 

 

