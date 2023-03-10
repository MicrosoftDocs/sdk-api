---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoProcessorOutputView
title: ID3D11VideoDevice::CreateVideoProcessorOutputView (d3d11.h)
description: Creates a resource view for a video processor, describing the output sample for the video processing operation.
helpviewer_keywords: ["CreateVideoProcessorOutputView","CreateVideoProcessorOutputView method [Media Foundation]","CreateVideoProcessorOutputView method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","CreateVideoProcessorOutputView method","ID3D11VideoDevice.CreateVideoProcessorOutputView","ID3D11VideoDevice::CreateVideoProcessorOutputView","d3d11/ID3D11VideoDevice::CreateVideoProcessorOutputView","mf.id3d11videodevice_createvideoprocessoroutputview"]
old-location: mf\id3d11videodevice_createvideoprocessoroutputview.htm
tech.root: mf
ms.assetid: EC7AFE44-877C-4FB0-9E61-FCD504A334D3
ms.date: 12/05/2018
ms.keywords: CreateVideoProcessorOutputView, CreateVideoProcessorOutputView method [Media Foundation], CreateVideoProcessorOutputView method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoProcessorOutputView method, ID3D11VideoDevice.CreateVideoProcessorOutputView, ID3D11VideoDevice::CreateVideoProcessorOutputView, d3d11/ID3D11VideoDevice::CreateVideoProcessorOutputView, mf.id3d11videodevice_createvideoprocessoroutputview
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
 - ID3D11VideoDevice::CreateVideoProcessorOutputView
 - d3d11/ID3D11VideoDevice::CreateVideoProcessorOutputView
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
 - ID3D11VideoDevice.CreateVideoProcessorOutputView
---

# ID3D11VideoDevice::CreateVideoProcessorOutputView


## -description

Creates a resource view for a video processor, describing the output sample for the video processing operation.

## -parameters

### -param pResource [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> interface of the output surface. The resource must be created with the <b>D3D11_BIND_RENDER_TARGET</b> flag. See <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_FLAG</a>.

### -param pEnum [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a> interface that specifies the video processor. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>.

### -param pDesc [in]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_output_view_desc">D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC</a> structure that describes the view.

### -param ppVPOView [out]

Receives a pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessoroutputview">ID3D11VideoProcessorOutputView</a> interface. The caller must release the resource. If this parameter is <b>NULL</b>, the method checks whether the view is supported, but does not create the view.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Set the <i>ppVPOView</i> parameter to <b>NULL</b> to test whether a view is supported.

Resources used for video processor output views must use the following <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_FLAG</a> combinations:

<ul>
<li>
<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_RENDER_TARGET</a> indicates that it can be used for a video processor output view. The following bind flags are allowed to be set with <b>D3D11_BIND_RENDER_TARGET</b>:<ul>
<li>
<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_VIDEO_ENCODER</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_SHADER_RESOURCE</a>
</li>
</ul>
</li>
<li>Other restrictions will apply such as:<ul>
<li>No multi-sampling is allowed.</li>
<li>The Texture2D must have been created using <a href="/windows/desktop/medfound/mf-sa-d3d11-usage">D3D11_USAGE_DEFAULT</a>.</li>
</ul>
</li>
<li>Some YUV formats can be supported as a video processor output view, but might not be supported as a 3D render target.  D3D11 will allow the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_RENDER_TARGET</a> flag for these formats, but <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview">CreateRenderTargetView</a> will not be allowed for these formats.</li>
</ul>
If stereo output is enabled, the output view must have 2 array elements.  Otherwise, it must only have a single array element.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>