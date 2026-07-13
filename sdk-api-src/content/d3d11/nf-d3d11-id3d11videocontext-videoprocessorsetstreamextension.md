---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamExtension
title: ID3D11VideoContext::VideoProcessorSetStreamExtension (d3d11.h)
description: Sets a driver-specific state on a video processing stream.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamExtension method","ID3D11VideoContext.VideoProcessorSetStreamExtension","ID3D11VideoContext::VideoProcessorSetStreamExtension","VideoProcessorSetStreamExtension","VideoProcessorSetStreamExtension method [Media Foundation]","VideoProcessorSetStreamExtension method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamExtension","mf.id3d11videocontext_videoprocessorsetstreamextension"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamextension.htm
tech.root: mf
ms.assetid: E6E1CF26-6A9F-42E1-8DA7-2AC76CE05906
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamExtension method, ID3D11VideoContext.VideoProcessorSetStreamExtension, ID3D11VideoContext::VideoProcessorSetStreamExtension, VideoProcessorSetStreamExtension, VideoProcessorSetStreamExtension method [Media Foundation], VideoProcessorSetStreamExtension method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamExtension, mf.id3d11videocontext_videoprocessorsetstreamextension
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
 - ID3D11VideoContext::VideoProcessorSetStreamExtension
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamExtension
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
 - ID3D11VideoContext.VideoProcessorSetStreamExtension
---

# ID3D11VideoContext::VideoProcessorSetStreamExtension


## -description

Sets a driver-specific state on a video processing stream.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pExtensionGuid [in]

A pointer to a GUID that identifies the operation. The meaning of this GUID is defined by the graphics driver.

### -param DataSize [in]

The size of the <i>pData</i> buffer, in bytes.

### -param pData [in]

A pointer to a buffer that contains private state data. The method passes this buffer directly to the driver without validation. It is the responsibility of the driver to validate the data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>