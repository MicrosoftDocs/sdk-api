---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorBlt
title: ID3D11VideoContext::VideoProcessorBlt (d3d11.h)
author: windows-sdk-content
description: Performs a video processing operation on one or more input samples and writes the result to a Direct3D surface.
old-location: mf\id3d11videocontext_videoprocessorblt.htm
tech.root: medfound
ms.assetid: D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorBlt method, ID3D11VideoContext.VideoProcessorBlt, ID3D11VideoContext::VideoProcessorBlt, VideoProcessorBlt, VideoProcessorBlt method [Media Foundation], VideoProcessorBlt method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorBlt, mf.id3d11videocontext_videoprocessorblt
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
 - ID3D11VideoContext.VideoProcessorBlt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorBlt


## -description


Performs a video processing operation on one or more input samples and writes the result to a Direct3D surface.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call the <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a> method.


### -param pView [in]

A pointer to the <a href="https://msdn.microsoft.com/D07829ED-2C1E-4150-A0A1-5CD95F30209F">ID3D11VideoProcessorOutputView</a> interface for the output surface. The output of the video processing operation will be written to this surface.


### -param OutputFrame [in]

The frame number of the output video frame, indexed from zero.




### -param StreamCount [in]

The number of input streams to process.


### -param pStreams [in]

A pointer to an array of <a href="https://msdn.microsoft.com/B861D00B-2FF2-4F8F-AD40-0EE6A9706A0C">D3D11_VIDEO_PROCESSOR_STREAM</a> structures that contain information about the input streams. The caller allocates the array and fills in each structure. The number of elements in the array is given in the <i>StreamCount</i> parameter.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The maximum value of <i>StreamCount</i> is given in the <b>MaxStreamStates</b> member of the <a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS</a> structure. The maximum number of streams that can be enabled at one time is given in the <b>MaxInputStreams</b> member of that structure.



If the output stereo mode is <b>TRUE</b>:

<ul>
<li>The output view must contain a texture array of two elements.</li>
<li>At least one stereo stream must be specified.</li>
<li>If multiple input streams are enabled, it is possible that one or more of the input streams may contain mono data.</li>
</ul>
Otherwise:

<ul>
<li>The output view must contain a single element.</li>
<li>The stereo format cannot be <a href="https://msdn.microsoft.com/77832DF2-821E-465C-80B6-46DDB2433791">D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO</a> .</li>
</ul>
This function does not honor a D3D11 predicate that may have been set.

If the application uses <a href="https://msdn.microsoft.com/4161fbeb-7f58-422c-a195-ea10f737fd0c">D3D11 quries</a>, this function may not be accounted for with <b>D3D11_QUERY_EVENT</b> and <b>D3D11_QUERY_TIMESTAMP</b> when using feature levels lower than 11.  <b>D3D11_QUERY_PIPELINE_STATISTICS</b> will not include this function for any feature level.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

