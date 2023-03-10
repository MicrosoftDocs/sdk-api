---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoProcessorInputView
title: ID3D11VideoDevice::CreateVideoProcessorInputView (d3d11.h)
description: Creates a resource view for a video processor, describing the input sample for the video processing operation.
helpviewer_keywords: ["CreateVideoProcessorInputView","CreateVideoProcessorInputView method [Media Foundation]","CreateVideoProcessorInputView method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","CreateVideoProcessorInputView method","ID3D11VideoDevice.CreateVideoProcessorInputView","ID3D11VideoDevice::CreateVideoProcessorInputView","d3d11/ID3D11VideoDevice::CreateVideoProcessorInputView","mf.id3d11videodevice_createvideoprocessorinputview"]
old-location: mf\id3d11videodevice_createvideoprocessorinputview.htm
tech.root: mf
ms.assetid: 3245D2AF-74A1-4068-A0BC-577FD42B353E
ms.date: 12/05/2018
ms.keywords: CreateVideoProcessorInputView, CreateVideoProcessorInputView method [Media Foundation], CreateVideoProcessorInputView method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoProcessorInputView method, ID3D11VideoDevice.CreateVideoProcessorInputView, ID3D11VideoDevice::CreateVideoProcessorInputView, d3d11/ID3D11VideoDevice::CreateVideoProcessorInputView, mf.id3d11videodevice_createvideoprocessorinputview
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
 - ID3D11VideoDevice::CreateVideoProcessorInputView
 - d3d11/ID3D11VideoDevice::CreateVideoProcessorInputView
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
 - ID3D11VideoDevice.CreateVideoProcessorInputView
---

# ID3D11VideoDevice::CreateVideoProcessorInputView


## -description

Creates a resource view for a video processor, describing the input sample for the video processing operation.

## -parameters

### -param pResource [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> interface of the input surface.

### -param pEnum [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a> interface that specifies the video processor. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>.

### -param pDesc [in]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_input_view_desc">D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC</a> structure that describes the view.

### -param ppVPIView [out]

Receives a pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorinputview">ID3D11VideoProcessorInputView</a> interface. The caller must release the resource. If this parameter is <b>NULL</b>, the method checks whether the view is supported, but does not create the view.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Set the <i>ppVPIView</i> parameter to <b>NULL</b> to test whether a view is supported.

The surface format is given in the <b>FourCC</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_input_view_desc">D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC</a> structure. The method fails if the video processor does not support this format as an input sample. An app must specify 0 when using 9_1, 9_2, or 9_3 feature levels. 

Resources used for video processor input views must use the following bind flag combinations:

<ul>
<li>Any combination of bind flags that includes <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_DECODER</a>,<b>D3D11_BIND_VIDEO_ENCODER</b>, <b>D3D11_BIND_RENDER_TARGET</b>, and <b>D3D11_BIND_UNORDERED_ACCESS_VIEW</b> can be used as for video processor input views (regardless of what other bind flags may be set).</li>
<li>Bind flags = 0 is also allowed for a video processor input view.</li>
<li>Other restrictions will apply such as:<ul>
<li>No multi-sampling is allowed.</li>
<li>The Texture2D must have been created using <a href="/windows/desktop/medfound/mf-sa-d3d11-usage">D3D11_USAGE_DEFAULT</a>.</li>
</ul>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>