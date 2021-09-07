---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoDecoderOutputView
title: ID3D11VideoDevice::CreateVideoDecoderOutputView (d3d11.h)
description: Creates a resource view for a video decoder, describing the output sample for the decoding operation.
helpviewer_keywords: ["CreateVideoDecoderOutputView","CreateVideoDecoderOutputView method [Media Foundation]","CreateVideoDecoderOutputView method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","CreateVideoDecoderOutputView method","ID3D11VideoDevice.CreateVideoDecoderOutputView","ID3D11VideoDevice::CreateVideoDecoderOutputView","d3d11/ID3D11VideoDevice::CreateVideoDecoderOutputView","mf.id3d11videodevice_createvideodecoderoutputview"]
old-location: mf\id3d11videodevice_createvideodecoderoutputview.htm
tech.root: mf
ms.assetid: 8A3D72CF-B641-4219-8C88-FCE5231CF2F6
ms.date: 12/05/2018
ms.keywords: CreateVideoDecoderOutputView, CreateVideoDecoderOutputView method [Media Foundation], CreateVideoDecoderOutputView method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoDecoderOutputView method, ID3D11VideoDevice.CreateVideoDecoderOutputView, ID3D11VideoDevice::CreateVideoDecoderOutputView, d3d11/ID3D11VideoDevice::CreateVideoDecoderOutputView, mf.id3d11videodevice_createvideodecoderoutputview
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
 - ID3D11VideoDevice::CreateVideoDecoderOutputView
 - d3d11/ID3D11VideoDevice::CreateVideoDecoderOutputView
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
 - ID3D11VideoDevice.CreateVideoDecoderOutputView
---

# ID3D11VideoDevice::CreateVideoDecoderOutputView


## -description

Creates a resource view for a video decoder, describing the output sample for the decoding operation.

## -parameters

### -param pResource [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> interface of the decoder surface. The resource must be created with the <b>D3D11_BIND_DECODER</b> flag. See <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_FLAG</a>.

### -param pDesc [in]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_output_view_desc">D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC</a> structure that describes the view.

### -param ppVDOVView [out]

Receives a pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview">ID3D11VideoDecoderOutputView</a> interface. The caller must release the interface. If this parameter is <b>NULL</b>, the method checks whether the view is supported, but does not create the view.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Set the <i>ppVDOVView</i> parameter to <b>NULL</b> to test whether a view is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>