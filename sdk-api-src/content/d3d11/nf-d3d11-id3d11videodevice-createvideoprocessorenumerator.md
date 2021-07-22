---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoProcessorEnumerator
title: ID3D11VideoDevice::CreateVideoProcessorEnumerator (d3d11.h)
description: Enumerates the video processor capabilities of the driver.
helpviewer_keywords: ["CreateVideoProcessorEnumerator","CreateVideoProcessorEnumerator method [Media Foundation]","CreateVideoProcessorEnumerator method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","CreateVideoProcessorEnumerator method","ID3D11VideoDevice.CreateVideoProcessorEnumerator","ID3D11VideoDevice::CreateVideoProcessorEnumerator","d3d11/ID3D11VideoDevice::CreateVideoProcessorEnumerator","mf.id3d11videodevice_createvideoprocessorenumerator"]
old-location: mf\id3d11videodevice_createvideoprocessorenumerator.htm
tech.root: mf
ms.assetid: 992C699D-A499-494E-AEDF-A6688CB14D70
ms.date: 12/05/2018
ms.keywords: CreateVideoProcessorEnumerator, CreateVideoProcessorEnumerator method [Media Foundation], CreateVideoProcessorEnumerator method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoProcessorEnumerator method, ID3D11VideoDevice.CreateVideoProcessorEnumerator, ID3D11VideoDevice::CreateVideoProcessorEnumerator, d3d11/ID3D11VideoDevice::CreateVideoProcessorEnumerator, mf.id3d11videodevice_createvideoprocessorenumerator
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
 - ID3D11VideoDevice::CreateVideoProcessorEnumerator
 - d3d11/ID3D11VideoDevice::CreateVideoProcessorEnumerator
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
 - ID3D11VideoDevice.CreateVideoProcessorEnumerator
---

# ID3D11VideoDevice::CreateVideoProcessorEnumerator


## -description

Enumerates the video processor capabilities of the driver.

## -parameters

### -param pDesc [in]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_content_desc">D3D11_VIDEO_PROCESSOR_CONTENT_DESC</a> structure that describes the video content.

### -param ppEnum [out]

Receives a pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To create the video processor device, pass the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a> pointer to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a> method.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>