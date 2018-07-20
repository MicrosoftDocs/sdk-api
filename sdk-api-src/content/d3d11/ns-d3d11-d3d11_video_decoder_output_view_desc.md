---
UID: NS:d3d11.D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
title: D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
author: windows-sdk-content
description: Describes a video decoder output view.
old-location: mf\d3d11_video_decoder_output_view_desc.htm
old-project: medfound
ms.assetid: 0A0C29C5-C3A3-43E7-86DA-1849AC276060
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC, D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC structure [Media Foundation], d3d11/D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC, mf.d3d11_video_decoder_output_view_desc
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
req.typenames: D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC structure


## -description


Describes a video decoder output view.


## -struct-fields




### -field DecodeProfile

The decoding profile. To get the list of profiles supported by the device, call the <a href="https://msdn.microsoft.com/8D958469-7FC3-4B4F-82BF-271662CF0088">ID3D11VideoDevice::GetVideoDecoderProfile</a> method.


### -field ViewDimension

The resource type of the view, specified as a member of the <a href="https://msdn.microsoft.com/079460EB-A7D4-4C8C-B7CA-9A6FFB3B0FA8">D3D11_VDOV_DIMENSION</a> enumeration.


### -field Texture2D

A <a href="https://msdn.microsoft.com/A25BB0AA-8CC9-4DA0-B4BE-8C107E9203F0">D3D11_TEX2D_VDOV</a> structure that identifies the texture resource for the output view.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/8A3D72CF-B641-4219-8C88-FCE5231CF2F6">ID3D11VideoDevice::CreateVideoDecoderOutputView</a>
 

 

