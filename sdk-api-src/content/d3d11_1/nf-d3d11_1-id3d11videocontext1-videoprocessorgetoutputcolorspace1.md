---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorGetOutputColorSpace1
title: ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1 (d3d11_1.h)
description: Gets the color space information for the video processor output surface.
helpviewer_keywords: ["ID3D11VideoContext1 interface [Media Foundation]","VideoProcessorGetOutputColorSpace1 method","ID3D11VideoContext1.VideoProcessorGetOutputColorSpace1","ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1","VideoProcessorGetOutputColorSpace1","VideoProcessorGetOutputColorSpace1 method [Media Foundation]","VideoProcessorGetOutputColorSpace1 method [Media Foundation]","ID3D11VideoContext1 interface","d3d11_1/ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1","mf.id3d11videocontext1_videoprocessorgetoutputcolorspace1"]
old-location: mf\id3d11videocontext1_videoprocessorgetoutputcolorspace1.htm
tech.root: mf
ms.assetid: 1B2BC801-CC5C-460C-A10E-CCDEE35A8E27
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorGetOutputColorSpace1 method, ID3D11VideoContext1.VideoProcessorGetOutputColorSpace1, ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1, VideoProcessorGetOutputColorSpace1, VideoProcessorGetOutputColorSpace1 method [Media Foundation], VideoProcessorGetOutputColorSpace1 method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1, mf.id3d11videocontext1_videoprocessorgetoutputcolorspace1
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1
 - d3d11_1/ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.VideoProcessorGetOutputColorSpace1
---

# ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1


## -description

Gets the color space information for the video processor output surface.

## -parameters

### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.

### -param pColorSpace [out]

Type: <b>DXGI_COLOR_SPACE_TYPE*</b>

A pointer to a <a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a> value that indicates the colorspace for the video processor output surface.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>