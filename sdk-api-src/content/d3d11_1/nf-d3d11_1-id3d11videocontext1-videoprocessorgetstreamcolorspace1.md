---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorGetStreamColorSpace1
title: ID3D11VideoContext1::VideoProcessorGetStreamColorSpace1 (d3d11_1.h)
description: Gets the color space information for the video processor input stream.helpviewer_keywords: ["ID3D11VideoContext1 interface [Media Foundation]","VideoProcessorGetStreamColorSpace1 method","ID3D11VideoContext1.VideoProcessorGetStreamColorSpace1","ID3D11VideoContext1::VideoProcessorGetStreamColorSpace1","VideoProcessorGetStreamColorSpace1","VideoProcessorGetStreamColorSpace1 method [Media Foundation]","VideoProcessorGetStreamColorSpace1 method [Media Foundation]","ID3D11VideoContext1 interface","d3d11_1/ID3D11VideoContext1::VideoProcessorGetStreamColorSpace1","mf.id3d11videocontext1_videoprocessorgetstreamcolorspace1"]
old-location: mf\id3d11videocontext1_videoprocessorgetstreamcolorspace1.htm
tech.root: medfound
ms.assetid: C9A53D81-C3E4-4B6F-9189-A58E40F8B7E7
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorGetStreamColorSpace1 method, ID3D11VideoContext1.VideoProcessorGetStreamColorSpace1, ID3D11VideoContext1::VideoProcessorGetStreamColorSpace1, VideoProcessorGetStreamColorSpace1, VideoProcessorGetStreamColorSpace1 method [Media Foundation], VideoProcessorGetStreamColorSpace1 method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorGetStreamColorSpace1, mf.id3d11videocontext1_videoprocessorgetstreamcolorspace1
f1_keywords:
- d3d11_1/ID3D11VideoContext1.VideoProcessorGetStreamColorSpace1
dev_langs:
- c++
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- COM
api_location:
- d3d11_1.h
api_name:
- ID3D11VideoContext1.VideoProcessorGetStreamColorSpace1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext1::VideoProcessorGetStreamColorSpace1


## -description


Gets the color space information for the video processor input stream.


## -parameters




### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.


### -param StreamIndex [in]

Type: <b>UINT</b>

An index identifying the input stream.


### -param pColorSpace [out]

Type: <b>DXGI_COLOR_SPACE_TYPE*</b>

A pointer to a  <a href="https://docs.microsoft.com/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a> value that specifies the colorspace for the video processor input stream.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>
 

 

