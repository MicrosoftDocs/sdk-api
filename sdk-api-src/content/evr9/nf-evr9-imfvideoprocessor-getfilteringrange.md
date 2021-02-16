---
UID: NF:evr9.IMFVideoProcessor.GetFilteringRange
title: IMFVideoProcessor::GetFilteringRange (evr9.h)
description: Retrieves the range of values for a specified image filter setting.
helpviewer_keywords: ["1e5f1635-51fe-4394-8a25-dcee3f55c711","GetFilteringRange","GetFilteringRange method [Media Foundation]","GetFilteringRange method [Media Foundation]","IMFVideoProcessor interface","IMFVideoProcessor interface [Media Foundation]","GetFilteringRange method","IMFVideoProcessor.GetFilteringRange","IMFVideoProcessor::GetFilteringRange","evr9/IMFVideoProcessor::GetFilteringRange","mf.imfvideoprocessor_getfilteringrange"]
old-location: mf\imfvideoprocessor_getfilteringrange.htm
tech.root: mf
ms.assetid: 1e5f1635-51fe-4394-8a25-dcee3f55c711
ms.date: 12/05/2018
ms.keywords: 1e5f1635-51fe-4394-8a25-dcee3f55c711, GetFilteringRange, GetFilteringRange method [Media Foundation], GetFilteringRange method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetFilteringRange method, IMFVideoProcessor.GetFilteringRange, IMFVideoProcessor::GetFilteringRange, evr9/IMFVideoProcessor::GetFilteringRange, mf.imfvideoprocessor_getfilteringrange
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
 - IMFVideoProcessor::GetFilteringRange
 - evr9/IMFVideoProcessor::GetFilteringRange
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
 - IMFVideoProcessor.GetFilteringRange
---

# IMFVideoProcessor::GetFilteringRange


## -description

Retrieves the range of values for a specified image filter setting.

## -parameters

### -param dwProperty [in]

The image filtering parameter to query. For a list of possible values, see <a href="/windows/desktop/medfound/dxva-image-filter-settings">DXVA Image Filter Settings</a>.

### -param pPropRange [out]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_valuerange">DXVA2_ValueRange</a> structure that receives range of values for the specified image filtering parameter.

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
<dt><b>DDERR_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The driver does not support this filter setting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>dwProperty</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
No video processor mode has been set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The specified operation is not available.

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

This method returns the range of values that the current video processor mode supports for the specified image filter setting.

This method fails if the video processor mode has not been set on the mixer. To select a video processor mode, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which image filters the driver supports, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">IMFVideoProcessor::GetVideoProcessorCaps</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>