---
UID: NF:evr9.IMFVideoProcessor.SetVideoProcessorMode
title: IMFVideoProcessor::SetVideoProcessorMode (evr9.h)
description: Sets the preferred video processor mode. The EVR will attempt to use this mode when playback starts.
helpviewer_keywords: ["4b353576-c8ee-4f73-9ee6-ba4545a6f4fc","IMFVideoProcessor interface [Media Foundation]","SetVideoProcessorMode method","IMFVideoProcessor.SetVideoProcessorMode","IMFVideoProcessor::SetVideoProcessorMode","SetVideoProcessorMode","SetVideoProcessorMode method [Media Foundation]","SetVideoProcessorMode method [Media Foundation]","IMFVideoProcessor interface","evr9/IMFVideoProcessor::SetVideoProcessorMode","mf.imfvideoprocessor_setvideoprocessormode"]
old-location: mf\imfvideoprocessor_setvideoprocessormode.htm
tech.root: mf
ms.assetid: 4b353576-c8ee-4f73-9ee6-ba4545a6f4fc
ms.date: 12/05/2018
ms.keywords: 4b353576-c8ee-4f73-9ee6-ba4545a6f4fc, IMFVideoProcessor interface [Media Foundation],SetVideoProcessorMode method, IMFVideoProcessor.SetVideoProcessorMode, IMFVideoProcessor::SetVideoProcessorMode, SetVideoProcessorMode, SetVideoProcessorMode method [Media Foundation], SetVideoProcessorMode method [Media Foundation],IMFVideoProcessor interface, evr9/IMFVideoProcessor::SetVideoProcessorMode, mf.imfvideoprocessor_setvideoprocessormode
f1_keywords:
- evr9/IMFVideoProcessor.SetVideoProcessorMode
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
api_name:
- IMFVideoProcessor.SetVideoProcessorMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoProcessor::SetVideoProcessorMode


## -description



Sets the preferred video processor mode. The EVR will attempt to use this mode when playback starts.




## -parameters




### -param lpMode [in]

Pointer to a GUID that identifies the video processor mode. To get a list of available modes, call <a href="https://docs.microsoft.com/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes">IMFVideoProcessor::GetAvailableVideoProcessorModes</a>.


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
<dt><b>D3DERR_INVALIDCALL</b></dt>
</dl>
</td>
<td width="60%">
The requested mode is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The mixer has already allocated Direct3D resources and cannot change modes.

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



Before calling this method, set the media type for the reference stream as follows:

<ul>
<li>
DirectShow EVR filter: Connect pin 0.

</li>
<li>
EVR media sink: Set the media type for stream 0.

</li>
<li>
Mixer (standalone): Set the media type for input stream 0 and set the media type for the output stream.

</li>
</ul>
Which modes are available might depend on the reference stream's media type.

Call this method before video playback begins.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>
 

 

