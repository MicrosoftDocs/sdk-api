---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamExtension
title: ID3D11VideoContext::VideoProcessorGetStreamExtension (d3d11.h)
description: Gets a driver-specific state for a video processing stream.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamExtension method","ID3D11VideoContext.VideoProcessorGetStreamExtension","ID3D11VideoContext::VideoProcessorGetStreamExtension","VideoProcessorGetStreamExtension","VideoProcessorGetStreamExtension method [Media Foundation]","VideoProcessorGetStreamExtension method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamExtension","mf.id3d11videocontext_videoprocessorgetstreamextension"]
old-location: mf\id3d11videocontext_videoprocessorgetstreamextension.htm
tech.root: mf
ms.assetid: 33A2DC3D-4B92-45B5-B67A-7F3AA55F061B
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamExtension method, ID3D11VideoContext.VideoProcessorGetStreamExtension, ID3D11VideoContext::VideoProcessorGetStreamExtension, VideoProcessorGetStreamExtension, VideoProcessorGetStreamExtension method [Media Foundation], VideoProcessorGetStreamExtension method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamExtension, mf.id3d11videocontext_videoprocessorgetstreamextension
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ID3D11VideoContext::VideoProcessorGetStreamExtension
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamExtension
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
 - ID3D11VideoContext.VideoProcessorGetStreamExtension
---

# ID3D11VideoContext::VideoProcessorGetStreamExtension


## -description

Gets a driver-specific state for a video processing stream.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pExtensionGuid [in]

A pointer to a GUID that identifies the state. The meaning of this GUID is defined by the graphics driver.

### -param DataSize [in]

The size of the <i>pData</i> buffer, in bytes.

### -param pData [out]

A pointer to a buffer that receives the private state data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>