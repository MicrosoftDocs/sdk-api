---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorGetBehaviorHints
title: ID3D11VideoContext1::VideoProcessorGetBehaviorHints (d3d11_1.h)
description: Returns driver hints that indicate which of the video processor operations are best performed using multi-plane overlay hardware rather than ID3D11VideoContext::VideoProcessorBlt method.
helpviewer_keywords: ["ID3D11VideoContext1 interface [Media Foundation]","VideoProcessorGetBehaviorHints method","ID3D11VideoContext1.VideoProcessorGetBehaviorHints","ID3D11VideoContext1::VideoProcessorGetBehaviorHints","VideoProcessorGetBehaviorHints","VideoProcessorGetBehaviorHints method [Media Foundation]","VideoProcessorGetBehaviorHints method [Media Foundation]","ID3D11VideoContext1 interface","d3d11_1/ID3D11VideoContext1::VideoProcessorGetBehaviorHints","mf.id3d11videocontext1_videoprocessorgetbehaviorhints"]
old-location: mf\id3d11videocontext1_videoprocessorgetbehaviorhints.htm
tech.root: mf
ms.assetid: DDA8B3DE-A9D2-48A5-ABEE-E3F7A0EEB965
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorGetBehaviorHints method, ID3D11VideoContext1.VideoProcessorGetBehaviorHints, ID3D11VideoContext1::VideoProcessorGetBehaviorHints, VideoProcessorGetBehaviorHints, VideoProcessorGetBehaviorHints method [Media Foundation], VideoProcessorGetBehaviorHints method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorGetBehaviorHints, mf.id3d11videocontext1_videoprocessorgetbehaviorhints
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
 - ID3D11VideoContext1::VideoProcessorGetBehaviorHints
 - d3d11_1/ID3D11VideoContext1::VideoProcessorGetBehaviorHints
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
 - ID3D11VideoContext1.VideoProcessorGetBehaviorHints
---

# ID3D11VideoContext1::VideoProcessorGetBehaviorHints


## -description

Returns driver hints that indicate which of the video processor operations are best performed using multi-plane overlay hardware rather than <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> method.

## -parameters

### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.

### -param OutputWidth [in]

Type: <b>UINT</b>

The width of the output stream.

### -param OutputHeight [in]

Type: <b>UINT</b>

The height of the output stream.

### -param OutputFormat [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

The format of the output stream.

### -param StreamCount [in]

Type: <b>UINT</b>

The number of input streams to process.

### -param pStreams [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_processor_stream_behavior_hint">D3D11_VIDEO_PROCESSOR_STREAM_BEHAVIOR_HINT</a>*</b>

An array of structures that specifies the format of each input stream and whether each stream should be used when computing behavior hints.

### -param pBehaviorHints [out]

Type: <b>UINT*</b>

A pointer to a bitwise OR combination of <a href="/windows/desktop/api/d3d11_1/ne-d3d11_1-d3d11_video_processor_behavior_hints">D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS</a> values indicating which video processor operations would best be performed using multi-plane overlay hardware rather than the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed or this function was called using an invalid calling pattern.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is insufficient memory to complete the operation.</td>
</tr>
</table>

## -remarks

This method computes the behavior hints using the current state of the video processor as set by the "SetOutput" and "SetStream" methods of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a> and <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>. You must set the proper state before calling this method to ensure that the returned hints contain useful data.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>