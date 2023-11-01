---
UID: NF:dxva2api.IDirectXVideoProcessor.VideoProcessBlt
title: IDirectXVideoProcessor::VideoProcessBlt (dxva2api.h)
description: Performs a video process operation on one or more input samples and writes the result to a Direct3D9 surface.
helpviewer_keywords: ["4a199ad3-621e-4594-a9f8-ad6cfd560cec","IDirectXVideoProcessor interface [Media Foundation]","VideoProcessBlt method","IDirectXVideoProcessor.VideoProcessBlt","IDirectXVideoProcessor::VideoProcessBlt","VideoProcessBlt","VideoProcessBlt method [Media Foundation]","VideoProcessBlt method [Media Foundation]","IDirectXVideoProcessor interface","dxva2api/IDirectXVideoProcessor::VideoProcessBlt","mf.idirectxvideoprocessor_videoprocessblt"]
old-location: mf\idirectxvideoprocessor_videoprocessblt.htm
tech.root: mf
ms.assetid: 4a199ad3-621e-4594-a9f8-ad6cfd560cec
ms.date: 12/05/2018
ms.keywords: 4a199ad3-621e-4594-a9f8-ad6cfd560cec, IDirectXVideoProcessor interface [Media Foundation],VideoProcessBlt method, IDirectXVideoProcessor.VideoProcessBlt, IDirectXVideoProcessor::VideoProcessBlt, VideoProcessBlt, VideoProcessBlt method [Media Foundation], VideoProcessBlt method [Media Foundation],IDirectXVideoProcessor interface, dxva2api/IDirectXVideoProcessor::VideoProcessBlt, mf.idirectxvideoprocessor_videoprocessblt
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IDirectXVideoProcessor::VideoProcessBlt
 - dxva2api/IDirectXVideoProcessor::VideoProcessBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoProcessor.VideoProcessBlt
---

# IDirectXVideoProcessor::VideoProcessBlt


## -description

Performs a video process operation on one or more input samples and writes the result to a Direct3D9 surface.

## -parameters

### -param pRenderTarget [in]

A pointer to the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface of a Direct3D surface. The output of the video processing operation will be written to this surface. The surface may be any of the following types:
          

<ul>
<li>A surface created by calling <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface">IDirectXVideoAccelerationService::CreateSurface</a> with the <b>DXVA2_VideoProcessRenderTarget</b> flag. You can also use the <b>DXVA2_VideoSoftwareRenderTarget</b> flag, but only when the device GUID is <b>DXVA2_VideoProcSoftwareDevice</b> (software video processing device).
              </li>
<li>A surface created from a Direct3D device with the <b>D3DUSAGE_RENDERTARGET</b> usage flag.
              </li>
<li>A Direct3D swap chain.
              </li>
</ul>

### -param pBltParams [in]

A pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams">DXVA2_VideoProcessBltParams</a> structure that describes the video processing operation to perform.

### -param pSamples [in]

A pointer to an array of <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample">DXVA2_VideoSample</a> structures that contain the input samples. There must be at least one element in the array.

The maximum number of input samples is given by the constant <b>MAX_DEINTERLACE_SURFACES</b>, defined in the header file dxva2api.h.

### -param NumSamples [in]

The number of elements in the <i>pSamples</i> array.

### -param pHandleComplete [out]

Reserved; set to <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_DRIVERINTERNALERROR</b></dt>
</dl>
</td>
<td width="60%">
Internal driver error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid arguments.

</td>
</tr>
</table>

## -remarks

When the method returns, the operation might not be complete.
      

If the method returns <b>E_INVALIDARG</b>, check for the following:

<ul>
<li>The number of input samples (<i>NumSamples</i>) must be less than or equal to <b>MAX_DEINTERLACE_SURFACES</b>. </li>
<li>The Direct3D surface must be a valid target for <b>VideoProcessBlt</b>. See the description of the <i>pRT</i> parameter for details.</li>
<li>The presentation time (<b>TargetFrame</b>) given in <i>pBltParams</i> must match the start and end times for the current picture from the primary stream. Specifically, it must be less than the end time and greater than or equal to the start time. Note that the first sample in <i>pSamples</i> might not be the current picture, if the <i>pSamples</i> array contains backward reference pictures. For more information, see <a href="/windows/desktop/medfound/dxva-video-processing">Input Sample Order</a>.</li>
<li>The target rectangle (<b>TargetRect</b>) given in <i>pBltParams</i> cannot be larger than the destination surface (<i>pRT</i>).</li>
<li>The  constriction size (<b>ConstrictionSize</b>) given in <i>pBltParams</i> cannot be less than zero or larger than the target rectangle.</li>
<li>The alpha component of the background color must be opqaue.</li>
<li>The ProcAmp values given in <i>pBltParams</i> must be valid. For any ProcAmp settings that are supported by the driver, these values must fall within the ranges returned by the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getprocamprange">IDirectXVideoProcessor::GetProcAmpRange</a> method.</li>
<li>The noise and detail filters given in <i>pBltParams</i> must be valid. For any filters that are supported by the driver, these values must fall within the ranges returned by the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-getfilterpropertyrange">IDirectXVideoProcessor::GetFilterPropertyRange</a> method.</li>
<li>The alpha value given in <i>pBltParams</i> must be in the range [0...1] inclusive.</li>
<li>For each input sample given in <i>pSamples</i>:<ul>
<li>The start time cannot be greater than the end time.</li>
<li>A valid <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> pointer must be provided.</li>
<li>The source rectangle cannot be larger than the input surface.</li>
<li>The destination rectangle cannot be larger than the destination surface.</li>
<li>The planar alpha must be in the range [0...1] inclusive.</li>
</ul>
</li>
<li> For all rectangles (source, destination, and target),  the rectangle cannot be inverted (left &gt; right or top &gt; bottom) or have negative values.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample">DXVA2_VideoSample</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor">IDirectXVideoProcessor</a>