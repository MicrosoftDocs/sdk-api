---
UID: NS:d3d11.D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
title: D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
author: windows-sdk-content
description: Describes a video decoder output view.
old-location: mf\d3d11_video_decoder_output_view_desc.htm
tech.root: medfound
ms.assetid: 0A0C29C5-C3A3-43E7-86DA-1849AC276060
ms.author: windowssdkdev
ms.date: 10/26/2018
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC
req.redist: 
---

# D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC structure


## -description


Describes a video decoder output view.


## -struct-fields




### -field DecodeProfile

The decoding profile. To get the list of profiles supported by the device, call the <a href="https://msdn.microsoft.com/en-us/library/Hh447795(v=VS.85).aspx">ID3D11VideoDevice::GetVideoDecoderProfile</a> method.


### -field ViewDimension

The resource type of the view, specified as a member of the <a href="https://msdn.microsoft.com/en-us/library/Hh447636(v=VS.85).aspx">D3D11_VDOV_DIMENSION</a> enumeration.


### -field Texture2D

A <a href="https://msdn.microsoft.com/en-us/library/Hh447633(v=VS.85).aspx">D3D11_TEX2D_VDOV</a> structure that identifies the texture resource for the output view.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447680(v=VS.85).aspx">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh447787(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoDecoderOutputView</a>
 

 

