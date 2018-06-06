---
UID: NF:evr9.IMFVideoProcessor.GetVideoProcessorCaps
title: IMFVideoProcessor::GetVideoProcessorCaps
author: windows-sdk-content
description: Retrieves the capabilities of a video processor mode.
old-location: mf\imfvideoprocessor_getvideoprocessorcaps.htm
old-project: medfound
ms.assetid: 9a02aed2-8225-4416-ae54-7ed51c67a149
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 9a02aed2-8225-4416-ae54-7ed51c67a149, GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetVideoProcessorCaps method, IMFVideoProcessor.GetVideoProcessorCaps, IMFVideoProcessor::GetVideoProcessorCaps, evr9/IMFVideoProcessor::GetVideoProcessorCaps, mf.imfvideoprocessor_getvideoprocessorcaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: evr9.h
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
tech.root: 
req.typenames: MFVideoAlphaBitmapFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoProcessor.GetVideoProcessorCaps
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoProcessor::GetVideoProcessorCaps


## -description



Retrieves the capabilities of a video processor mode.




## -parameters




### -param lpVideoProcessorMode [in]

Pointer to a GUID that identifies the video processor mode. To get a list of available modes, call <a href="https://msdn.microsoft.com/1004341d-d39b-4032-a027-39e35ecab635">IMFVideoProcessor::GetAvailableVideoProcessorModes</a>.


### -param lpVideoProcessorCaps [out]

Pointer to a <a href="https://msdn.microsoft.com/cff01719-e653-4ea1-a177-9a6948b0da56">DXVA2_VideoProcessorCaps</a> structure that receives the capabilities.


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
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The media type for the reference stream is not set.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, you must set the media type for the reference stream.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/0a63c4f8-eb32-4f0c-b69b-0c16243f2f21">IMFVideoProcessor</a>
 

 

