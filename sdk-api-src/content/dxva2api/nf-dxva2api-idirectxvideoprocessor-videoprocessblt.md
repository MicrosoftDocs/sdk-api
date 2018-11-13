---
UID: NF:dxva2api.IDirectXVideoProcessor.VideoProcessBlt
title: IDirectXVideoProcessor::VideoProcessBlt
author: windows-sdk-content
description: Performs a video process operation on one or more input samples and writes the result to a Direct3D9 surface.
old-location: mf\idirectxvideoprocessor_videoprocessblt.htm
tech.root: medfound
ms.assetid: 4a199ad3-621e-4594-a9f8-ad6cfd560cec
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 4a199ad3-621e-4594-a9f8-ad6cfd560cec, IDirectXVideoProcessor interface [Media Foundation],VideoProcessBlt method, IDirectXVideoProcessor.VideoProcessBlt, IDirectXVideoProcessor::VideoProcessBlt, VideoProcessBlt, VideoProcessBlt method [Media Foundation], VideoProcessBlt method [Media Foundation],IDirectXVideoProcessor interface, dxva2api/IDirectXVideoProcessor::VideoProcessBlt, mf.idirectxvideoprocessor_videoprocessblt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoProcessor.VideoProcessBlt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoProcessor::VideoProcessBlt


## -description


Performs a video process operation on one or more input samples and writes the result to a Direct3D9 surface.
        


## -parameters




### -param pRenderTarget

TBD


### -param pBltParams [in]

A pointer to a <a href="https://msdn.microsoft.com/6929fa8b-3cab-4d4e-ab2a-a3059b00905f">DXVA2_VideoProcessBltParams</a> structure that describes the video processing operation to perform.
          


### -param pSamples [in]

A pointer to an array of <a href="https://msdn.microsoft.com/040ade10-8573-4375-829d-938efa750a12">DXVA2_VideoSample</a> structures that contain the input samples. There must be at least one element in the array.

The maximum number of input samples is given by the constant <b>MAX_DEINTERLACE_SURFACES</b>, defined in the header file dxva2api.h.


### -param NumSamples [in]

The number of elements in the <i>pSamples</i> array.
          


### -param pHandleComplete [out]

Reserved; set to <b>NULL</b>.
          


#### - pRT [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a> interface of a Direct3D surface. The output of the video processing operation will be written to this surface. The surface may be any of the following types:
          

<ul>
<li>A surface created by calling <a href="https://msdn.microsoft.com/34ed2029-7c79-45ce-962d-df4970babb23">IDirectXVideoAccelerationService::CreateSurface</a> with the <b>DXVA2_VideoProcessRenderTarget</b> flag. You can also use the <b>DXVA2_VideoSoftwareRenderTarget</b> flag, but only when the device GUID is <b>DXVA2_VideoProcSoftwareDevice</b> (software video processing device).
              </li>
<li>A surface created from a Direct3D device with the <b>D3DUSAGE_RENDERTARGET</b> usage flag.
              </li>
<li>A Direct3D swap chain.
              </li>
</ul>

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
<li>The presentation time (<b>TargetFrame</b>) given in <i>pBltParams</i> must match the start and end times for the current picture from the primary stream. Specifically, it must be less than the end time and greater than or equal to the start time. Note that the first sample in <i>pSamples</i> might not be the current picture, if the <i>pSamples</i> array contains backward reference pictures. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Cc307964(v=VS.85).aspx">Input Sample Order</a>.</li>
<li>The target rectangle (<b>TargetRect</b>) given in <i>pBltParams</i> cannot be larger than the destination surface (<i>pRT</i>).</li>
<li>The  constriction size (<b>ConstrictionSize</b>) given in <i>pBltParams</i> cannot be less than zero or larger than the target rectangle.</li>
<li>The alpha component of the background color must be opqaue.</li>
<li>The ProcAmp values given in <i>pBltParams</i> must be valid. For any ProcAmp settings that are supported by the driver, these values must fall within the ranges returned by the <a href="https://msdn.microsoft.com/e15c8425-7a0b-4d03-b2da-467c800c57c2">IDirectXVideoProcessor::GetProcAmpRange</a> method.</li>
<li>The noise and detail filters given in <i>pBltParams</i> must be valid. For any filters that are supported by the driver, these values must fall within the ranges returned by the <a href="https://msdn.microsoft.com/550c426b-a194-4ed6-9a90-b79a93e79322">IDirectXVideoProcessor::GetFilterPropertyRange</a> method.</li>
<li>The alpha value given in <i>pBltParams</i> must be in the range [0...1] inclusive.</li>
<li>For each input sample given in <i>pSamples</i>:<ul>
<li>The start time cannot be greater than the end time.</li>
<li>A valid <a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a> pointer must be provided.</li>
<li>The source rectangle cannot be larger than the input surface.</li>
<li>The destination rectangle cannot be larger than than the destination surface.</li>
<li>The planar alpha must be in the range [0...1] inclusive.</li>
</ul>
</li>
<li> For all rectangles (source, destination, and target),  the rectangle cannot be inverted (left &gt; right or top &gt; bottom) or have negative values.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/040ade10-8573-4375-829d-938efa750a12">DXVA2_VideoSample</a>



<a href="https://msdn.microsoft.com/a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5">IDirectXVideoProcessor</a>
 

 

