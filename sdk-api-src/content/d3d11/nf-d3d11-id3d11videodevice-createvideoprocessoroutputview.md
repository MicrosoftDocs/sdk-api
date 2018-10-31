---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoProcessorOutputView
title: ID3D11VideoDevice::CreateVideoProcessorOutputView
author: windows-sdk-content
description: Creates a resource view for a video processor, describing the output sample for the video processing operation.
old-location: mf\id3d11videodevice_createvideoprocessoroutputview.htm
tech.root: medfound
ms.assetid: EC7AFE44-877C-4FB0-9E61-FCD504A334D3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateVideoProcessorOutputView, CreateVideoProcessorOutputView method [Media Foundation], CreateVideoProcessorOutputView method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoProcessorOutputView method, ID3D11VideoDevice.CreateVideoProcessorOutputView, ID3D11VideoDevice::CreateVideoProcessorOutputView, d3d11/ID3D11VideoDevice::CreateVideoProcessorOutputView, mf.id3d11videodevice_createvideoprocessoroutputview
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDevice.CreateVideoProcessorOutputView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDevice::CreateVideoProcessorOutputView


## -description


Creates a resource view for a video processor, describing the output sample for the video processing operation.


## -parameters




### -param pResource [in]

A pointer to the <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> interface of the output surface. The resource must be created with the <b>D3D11_BIND_RENDER_TARGET</b> flag. See <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_FLAG</a>.


### -param pEnum [in]

A pointer to the <a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a> interface that specifies the video processor. To get this pointer, call <a href="https://msdn.microsoft.com/992C699D-A499-494E-AEDF-A6688CB14D70">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>.


### -param pDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/8E0D44C1-220C-4E70-8A60-591AEBC16A2B">D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC</a> structure that describes the view.


### -param ppVPOView [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/D07829ED-2C1E-4150-A0A1-5CD95F30209F">ID3D11VideoProcessorOutputView</a> interface. The caller must release the resource. If this parameter is <b>NULL</b>, the method checks whether the view is supported, but does not create the view. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Set the <i>ppVPOView</i> parameter to <b>NULL</b> to test whether a view is supported.

Resources used for video processor output views must use the following <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_FLAG</a> combinations:

<ul>
<li>
<a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_RENDER_TARGET</a> indicates that it can be used for a video processor output view. The following bind flags are allowed to be set with <b>D3D11_BIND_RENDER_TARGET</b>:<ul>
<li>
<a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_VIDEO_ENCODER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_SHADER_RESOURCE</a>
</li>
</ul>
</li>
<li>Other restrictions will apply such as:<ul>
<li>No multi-sampling is allowed.</li>
<li>The Texture2D must have been created using <a href="https://msdn.microsoft.com/E9A415FA-74BF-4822-BB0E-D8AAA7D73664">D3D11_USAGE_DEFAULT</a>.</li>
</ul>
</li>
<li>Some YUV formats can be supported as a video processor output view, but might not be supported as a 3D render target.  D3D11 will allow the <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_RENDER_TARGET</a> flag for these formats, but <a href="https://msdn.microsoft.com/e757c959-f0ac-44c3-8226-b9f0b1c2a031">CreateRenderTargetView</a> will not be allowed for these formats.</li>
</ul>
If stereo output is enabled, the output view must have 2 array elements.  Otherwise, it must only have a single array element.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

