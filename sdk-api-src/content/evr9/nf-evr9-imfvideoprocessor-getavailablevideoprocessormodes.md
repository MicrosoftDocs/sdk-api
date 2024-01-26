---
UID: NF:evr9.IMFVideoProcessor.GetAvailableVideoProcessorModes
title: IMFVideoProcessor::GetAvailableVideoProcessorModes (evr9.h)
description: Retrieves the video processor modes that the video driver supports.
helpviewer_keywords: ["1004341d-d39b-4032-a027-39e35ecab635","GetAvailableVideoProcessorModes","GetAvailableVideoProcessorModes method [Media Foundation]","GetAvailableVideoProcessorModes method [Media Foundation]","IMFVideoProcessor interface","IMFVideoProcessor interface [Media Foundation]","GetAvailableVideoProcessorModes method","IMFVideoProcessor.GetAvailableVideoProcessorModes","IMFVideoProcessor::GetAvailableVideoProcessorModes","evr9/IMFVideoProcessor::GetAvailableVideoProcessorModes","mf.imfvideoprocessor_getavailablevideoprocessormodes"]
old-location: mf\imfvideoprocessor_getavailablevideoprocessormodes.htm
tech.root: mfarchive
ms.assetid: 1004341d-d39b-4032-a027-39e35ecab635
ms.date: 12/05/2018
ms.keywords: 1004341d-d39b-4032-a027-39e35ecab635, GetAvailableVideoProcessorModes, GetAvailableVideoProcessorModes method [Media Foundation], GetAvailableVideoProcessorModes method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetAvailableVideoProcessorModes method, IMFVideoProcessor.GetAvailableVideoProcessorModes, IMFVideoProcessor::GetAvailableVideoProcessorModes, evr9/IMFVideoProcessor::GetAvailableVideoProcessorModes, mf.imfvideoprocessor_getavailablevideoprocessormodes
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
 - IMFVideoProcessor::GetAvailableVideoProcessorModes
 - evr9/IMFVideoProcessor::GetAvailableVideoProcessorModes
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
 - IMFVideoProcessor.GetAvailableVideoProcessorModes
archived: true
---

# IMFVideoProcessor::GetAvailableVideoProcessorModes


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Retrieves the video processor modes that the video driver supports.

## -parameters

### -param lpdwNumProcessingModes [in, out]

Receives the number of video processor modes.

### -param ppVideoProcessingModes [out]

Receives a pointer to an array of GUIDs. The number of elements in the array is returned in the <i>lpdwNumProcessingModes</i> parameter. The caller must release the memory for the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.

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

Video processor modes are identified by GUID. For a list of predefined GUIDs, see <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>. A driver can define additional vendor-specific GUIDs. To get the capabilities of each mode, pass the GUID to the <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">IMFVideoProcessor::GetVideoProcessorCaps</a> method.

Before calling this method, you must set the media type for the reference stream. Which modes are available might depend on the media type of the reference stream.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>