---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_CONTENT_DESC
title: D3D11_VIDEO_PROCESSOR_CONTENT_DESC
author: windows-driver-content
description: Describes a video stream for a video processor.
old-location: mf\d3d11_video_processor_content_desc.htm
old-project: medfound
ms.assetid: A1649897-B368-4D03-9A08-630C8C59E44A
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_CONTENT_DESC, D3D11_VIDEO_PROCESSOR_CONTENT_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_CONTENT_DESC, mf.d3d11_video_processor_content_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VIDEO_PROCESSOR_CONTENT_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11.h
api_name:
-	D3D11_VIDEO_PROCESSOR_CONTENT_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_PROCESSOR_CONTENT_DESC structure


## -description


Describes a video stream for a video processor.


## -struct-fields




### -field InputFrameFormat

A member of the <a href="https://msdn.microsoft.com/D0C0C58C-8BBC-4C2C-BD0B-4244211E7E06">D3D11_VIDEO_FRAME_FORMAT</a> enumeration that describes how the video stream is interlaced.


### -field InputFrameRate

The frame rate of the input video stream, specified as a <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure.




### -field InputWidth

The width of the input frames, in pixels.


### -field InputHeight

The height of the input frames, in pixels.


### -field OutputFrameRate

The frame rate of the output video stream, specified as a <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure.




### -field OutputWidth

The width of the output frames, in pixels.




### -field OutputHeight

The height of the output frames, in pixels.


### -field Usage

A member of the <a href="https://msdn.microsoft.com/11657847-FFDB-42EA-9A29-FDC1F92DF039">D3D11_VIDEO_USAGE</a> enumeration that describes how the video processor will be used. The value indicates the desired trade-off between speed and video quality. The driver uses this flag as a hint when it creates the video processor.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/992C699D-A499-494E-AEDF-A6688CB14D70">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>
 

 

