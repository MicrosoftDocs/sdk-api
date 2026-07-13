---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorFilterRange
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange (d3d11.h)
description: Gets the range of values for an image filter.
helpviewer_keywords: ["GetVideoProcessorFilterRange","GetVideoProcessorFilterRange method [Media Foundation]","GetVideoProcessorFilterRange method [Media Foundation]","ID3D11VideoProcessorEnumerator interface","ID3D11VideoProcessorEnumerator interface [Media Foundation]","GetVideoProcessorFilterRange method","ID3D11VideoProcessorEnumerator.GetVideoProcessorFilterRange","ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange","d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange","mf.id3d11videoprocessorenumerator_getvideoprocessorfilterrange"]
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorfilterrange.htm
tech.root: mf
ms.assetid: F43A01D7-A0FE-4509-B3B2-094B09A7F04A
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorFilterRange, GetVideoProcessorFilterRange method [Media Foundation], GetVideoProcessorFilterRange method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],GetVideoProcessorFilterRange method, ID3D11VideoProcessorEnumerator.GetVideoProcessorFilterRange, ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange, mf.id3d11videoprocessorenumerator_getvideoprocessorfilterrange
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
 - ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange
 - d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange
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
 - ID3D11VideoProcessorEnumerator.GetVideoProcessorFilterRange
---

# ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange


## -description

Gets the range of values for an image filter.

## -parameters

### -param Filter [in]

The type of image filter, specified as a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_filter">D3D11_VIDEO_PROCESSOR_FILTER</a> value.

### -param pRange [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_filter_range">D3D11_VIDEO_PROCESSOR_FILTER_RANGE</a> structure. The method fills the structure with the range of values for the specified filter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a>