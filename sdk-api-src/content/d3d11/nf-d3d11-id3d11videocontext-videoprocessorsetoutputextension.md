---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputExtension
title: ID3D11VideoContext::VideoProcessorSetOutputExtension (d3d11.h)
description: Sets a driver-specific video processing state.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetOutputExtension method","ID3D11VideoContext.VideoProcessorSetOutputExtension","ID3D11VideoContext::VideoProcessorSetOutputExtension","VideoProcessorSetOutputExtension","VideoProcessorSetOutputExtension method [Media Foundation]","VideoProcessorSetOutputExtension method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetOutputExtension","mf.id3d11videocontext_videoprocessorsetoutputextension"]
old-location: mf\id3d11videocontext_videoprocessorsetoutputextension.htm
tech.root: mf
ms.assetid: 38279599-09C8-4BB1-8946-0B066D96E22B
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputExtension method, ID3D11VideoContext.VideoProcessorSetOutputExtension, ID3D11VideoContext::VideoProcessorSetOutputExtension, VideoProcessorSetOutputExtension, VideoProcessorSetOutputExtension method [Media Foundation], VideoProcessorSetOutputExtension method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputExtension, mf.id3d11videocontext_videoprocessorsetoutputextension
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
 - ID3D11VideoContext::VideoProcessorSetOutputExtension
 - d3d11/ID3D11VideoContext::VideoProcessorSetOutputExtension
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
 - ID3D11VideoContext.VideoProcessorSetOutputExtension
---

# ID3D11VideoContext::VideoProcessorSetOutputExtension


## -description

Sets a driver-specific video processing state.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

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