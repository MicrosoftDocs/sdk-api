---
UID: NS:d3d11.D3D11_VIDEO_DECODER_DESC
title: D3D11_VIDEO_DECODER_DESC
author: windows-sdk-content
description: Describes a video stream for a Microsoft Direct3D 11 video decoder or video processor.
old-location: mf\d3d11_video_decoder_desc.htm
old-project: medfound
ms.assetid: 668D994C-B875-4666-B940-1052A6DE6AA1
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: D3D11_VIDEO_DECODER_DESC, D3D11_VIDEO_DECODER_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_DECODER_DESC, mf.d3d11_video_decoder_desc
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VIDEO_DECODER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_DECODER_DESC structure


## -description


Describes a video stream for a Microsoft Direct3D 11 video decoder or video processor. 




## -struct-fields




### -field Guid

The decoding profile. To get the list of profiles supported by the device, call the <a href="https://msdn.microsoft.com/8D958469-7FC3-4B4F-82BF-271662CF0088">ID3D11VideoDevice::GetVideoDecoderProfile</a> method.


### -field SampleWidth

The width of the video frame, in pixels. 




### -field SampleHeight

The height of the video frame, in pixels. 




### -field OutputFormat

The output surface format, specified as a <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> value.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

