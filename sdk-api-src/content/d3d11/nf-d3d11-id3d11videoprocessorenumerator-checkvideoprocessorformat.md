---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.CheckVideoProcessorFormat
title: ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat (d3d11.h)
description: Queries whether the video processor supports a specified video format.
helpviewer_keywords: ["CheckVideoProcessorFormat","CheckVideoProcessorFormat method [Media Foundation]","CheckVideoProcessorFormat method [Media Foundation]","ID3D11VideoProcessorEnumerator interface","ID3D11VideoProcessorEnumerator interface [Media Foundation]","CheckVideoProcessorFormat method","ID3D11VideoProcessorEnumerator.CheckVideoProcessorFormat","ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat","d3d11/ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat","mf.id3d11videoprocessorenumerator_checkvideoprocessorformat"]
old-location: mf\id3d11videoprocessorenumerator_checkvideoprocessorformat.htm
tech.root: mf
ms.assetid: 75DE439B-6849-4413-BF7D-0EBADA96F097
ms.date: 12/05/2018
ms.keywords: CheckVideoProcessorFormat, CheckVideoProcessorFormat method [Media Foundation], CheckVideoProcessorFormat method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],CheckVideoProcessorFormat method, ID3D11VideoProcessorEnumerator.CheckVideoProcessorFormat, ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat, d3d11/ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat, mf.id3d11videoprocessorenumerator_checkvideoprocessorformat
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
 - ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat
 - d3d11/ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat
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
 - ID3D11VideoProcessorEnumerator.CheckVideoProcessorFormat
---

# ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat


## -description

Queries whether the video processor supports a specified video format.

## -parameters

### -param Format [in]

The video format to query, specified as a <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> value.

### -param pFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_support">D3D11_VIDEO_PROCESSOR_FORMAT_SUPPORT</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a>