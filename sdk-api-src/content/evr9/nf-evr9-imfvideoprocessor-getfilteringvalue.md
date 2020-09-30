---
UID: NF:evr9.IMFVideoProcessor.GetFilteringValue
title: IMFVideoProcessor::GetFilteringValue (evr9.h)
description: Retrieves the current setting for an image filter.
helpviewer_keywords: ["1c8d6836-ca62-4d26-be4e-572dc6ff994d","GetFilteringValue","GetFilteringValue method [Media Foundation]","GetFilteringValue method [Media Foundation]","IMFVideoProcessor interface","IMFVideoProcessor interface [Media Foundation]","GetFilteringValue method","IMFVideoProcessor.GetFilteringValue","IMFVideoProcessor::GetFilteringValue","evr9/IMFVideoProcessor::GetFilteringValue","mf.imfvideoprocessor_getfilteringvalue"]
old-location: mf\imfvideoprocessor_getfilteringvalue.htm
tech.root: mf
ms.assetid: 1c8d6836-ca62-4d26-be4e-572dc6ff994d
ms.date: 12/05/2018
ms.keywords: 1c8d6836-ca62-4d26-be4e-572dc6ff994d, GetFilteringValue, GetFilteringValue method [Media Foundation], GetFilteringValue method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetFilteringValue method, IMFVideoProcessor.GetFilteringValue, IMFVideoProcessor::GetFilteringValue, evr9/IMFVideoProcessor::GetFilteringValue, mf.imfvideoprocessor_getfilteringvalue
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
 - IMFVideoProcessor::GetFilteringValue
 - evr9/IMFVideoProcessor::GetFilteringValue
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
 - IMFVideoProcessor.GetFilteringValue
---

# IMFVideoProcessor::GetFilteringValue


## -description

Retrieves the current setting for an image filter.

## -parameters

### -param dwProperty [in]

The filter setting to query. For a list of possible values, see <a href="/windows/desktop/medfound/dxva-image-filter-settings">DXVA Image Filter Settings</a>.

### -param pValue [out]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_fixed32">DXVA2_Fixed32</a> structure that receives the current value.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwProperty</i> is invalid.

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

Until the mixer's video processor mode is set, the returned values are all zero. After the processor mode is set, the returned values reflect the current mode. To select a video processor mode, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which image filters the driver supports, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">IMFVideoProcessor::GetVideoProcessorCaps</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>