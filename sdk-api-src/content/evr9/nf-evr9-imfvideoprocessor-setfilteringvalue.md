---
UID: NF:evr9.IMFVideoProcessor.SetFilteringValue
title: IMFVideoProcessor::SetFilteringValue (evr9.h)
description: Sets a parameter for an image filter.
helpviewer_keywords: ["IMFVideoProcessor interface [Media Foundation]","SetFilteringValue method","IMFVideoProcessor.SetFilteringValue","IMFVideoProcessor::SetFilteringValue","SetFilteringValue","SetFilteringValue method [Media Foundation]","SetFilteringValue method [Media Foundation]","IMFVideoProcessor interface","cb3c9516-2083-4c9d-b583-fc561f977ed5","evr9/IMFVideoProcessor::SetFilteringValue","mf.imfvideoprocessor_setfilteringvalue"]
old-location: mf\imfvideoprocessor_setfilteringvalue.htm
tech.root: mfarchive
ms.assetid: cb3c9516-2083-4c9d-b583-fc561f977ed5
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessor interface [Media Foundation],SetFilteringValue method, IMFVideoProcessor.SetFilteringValue, IMFVideoProcessor::SetFilteringValue, SetFilteringValue, SetFilteringValue method [Media Foundation], SetFilteringValue method [Media Foundation],IMFVideoProcessor interface, cb3c9516-2083-4c9d-b583-fc561f977ed5, evr9/IMFVideoProcessor::SetFilteringValue, mf.imfvideoprocessor_setfilteringvalue
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
 - IMFVideoProcessor::SetFilteringValue
 - evr9/IMFVideoProcessor::SetFilteringValue
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
 - IMFVideoProcessor.SetFilteringValue
archived: true
---

# IMFVideoProcessor::SetFilteringValue


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets a parameter for an image filter.

## -parameters

### -param dwProperty [in]

The image filtering parameter to set. For a list of possible values, see <a href="/windows/desktop/medfound/dxva-image-filter-settings">DXVA Image Filter Settings</a>.

### -param pValue [in]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_fixed32">DXVA2_Fixed32</a> structure that specifies the new value. To get the valid range of values for each parameter, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange">IMFVideoProcessor::GetFilteringRange</a>.

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

Before calling this method, set the video processor mode. To select a video processor mode, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which image filters the driver supports, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">IMFVideoProcessor::GetVideoProcessorCaps</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>