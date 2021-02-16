---
UID: NF:evr9.IMFVideoProcessor.GetVideoProcessorMode
title: IMFVideoProcessor::GetVideoProcessorMode (evr9.h)
description: Retrieves the application's preferred video processor mode. To set the preferred mode, call IMFVideoProcessor::SetVideoProcessorMode.
helpviewer_keywords: ["GetVideoProcessorMode","GetVideoProcessorMode method [Media Foundation]","GetVideoProcessorMode method [Media Foundation]","IMFVideoProcessor interface","IMFVideoProcessor interface [Media Foundation]","GetVideoProcessorMode method","IMFVideoProcessor.GetVideoProcessorMode","IMFVideoProcessor::GetVideoProcessorMode","df45c379-f525-4018-b2c2-88a52b13dff5","evr9/IMFVideoProcessor::GetVideoProcessorMode","mf.imfvideoprocessor_getvideoprocessormode"]
old-location: mf\imfvideoprocessor_getvideoprocessormode.htm
tech.root: mf
ms.assetid: df45c379-f525-4018-b2c2-88a52b13dff5
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorMode, GetVideoProcessorMode method [Media Foundation], GetVideoProcessorMode method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetVideoProcessorMode method, IMFVideoProcessor.GetVideoProcessorMode, IMFVideoProcessor::GetVideoProcessorMode, df45c379-f525-4018-b2c2-88a52b13dff5, evr9/IMFVideoProcessor::GetVideoProcessorMode, mf.imfvideoprocessor_getvideoprocessormode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoProcessor::GetVideoProcessorMode
 - evr9/IMFVideoProcessor::GetVideoProcessorMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoProcessor.GetVideoProcessorMode
---

# IMFVideoProcessor::GetVideoProcessorMode


## -description

Retrieves the application's preferred video processor mode. To set the preferred mode, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode">IMFVideoProcessor::SetVideoProcessorMode</a>.

## -parameters

### -param lpMode [out]

Receives a GUID that identifies the preferred video processor mode.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The application has not specified a preferred video processor mode.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>