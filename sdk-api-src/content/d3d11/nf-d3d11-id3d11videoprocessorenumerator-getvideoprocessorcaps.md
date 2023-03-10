---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorCaps
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps (d3d11.h)
description: Gets the capabilities of the video processor.
helpviewer_keywords: ["GetVideoProcessorCaps","GetVideoProcessorCaps method [Media Foundation]","GetVideoProcessorCaps method [Media Foundation]","ID3D11VideoProcessorEnumerator interface","ID3D11VideoProcessorEnumerator interface [Media Foundation]","GetVideoProcessorCaps method","ID3D11VideoProcessorEnumerator.GetVideoProcessorCaps","ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps","d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps","mf.id3d11videoprocessorenumerator_getvideoprocessorcaps"]
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorcaps.htm
tech.root: mf
ms.assetid: BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],GetVideoProcessorCaps method, ID3D11VideoProcessorEnumerator.GetVideoProcessorCaps, ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps, mf.id3d11videoprocessorenumerator_getvideoprocessorcaps
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps
 - d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoProcessorEnumerator.GetVideoProcessorCaps
---

# ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps


## -description

Gets the capabilities of the video processor.

## -parameters

### -param pCaps [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a> structure that receives the capabilities.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a>