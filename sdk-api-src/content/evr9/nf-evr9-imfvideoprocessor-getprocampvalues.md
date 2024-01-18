---
UID: NF:evr9.IMFVideoProcessor.GetProcAmpValues
title: IMFVideoProcessor::GetProcAmpValues (evr9.h)
description: Retrieves the current settings for one or more color adjustment (ProcAmp) settings.
helpviewer_keywords: ["GetProcAmpValues","GetProcAmpValues method [Media Foundation]","GetProcAmpValues method [Media Foundation]","IMFVideoProcessor interface","IMFVideoProcessor interface [Media Foundation]","GetProcAmpValues method","IMFVideoProcessor.GetProcAmpValues","IMFVideoProcessor::GetProcAmpValues","d1d6f6a4-fe3b-4acf-a004-d02ece41a302","evr9/IMFVideoProcessor::GetProcAmpValues","mf.imfvideoprocessor_getprocampvalues"]
old-location: mf\imfvideoprocessor_getprocampvalues.htm
tech.root: mfarchive
ms.assetid: d1d6f6a4-fe3b-4acf-a004-d02ece41a302
ms.date: 12/05/2018
ms.keywords: GetProcAmpValues, GetProcAmpValues method [Media Foundation], GetProcAmpValues method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetProcAmpValues method, IMFVideoProcessor.GetProcAmpValues, IMFVideoProcessor::GetProcAmpValues, d1d6f6a4-fe3b-4acf-a004-d02ece41a302, evr9/IMFVideoProcessor::GetProcAmpValues, mf.imfvideoprocessor_getprocampvalues
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
 - IMFVideoProcessor::GetProcAmpValues
 - evr9/IMFVideoProcessor::GetProcAmpValues
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
 - IMFVideoProcessor.GetProcAmpValues
archived: true
---

# IMFVideoProcessor::GetProcAmpValues


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Retrieves the current settings for one or more color adjustment (ProcAmp) settings.

## -parameters

### -param dwFlags [in]

Bitwise <b>OR</b> of one or more flags, specifying which operations to query. For a list of flags, see <a href="/windows/desktop/medfound/procamp-settings">ProcAmp Settings</a>.

### -param Values [out]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_procampvalues">DXVA2_ProcAmpValues</a> structure. The method fills the structure with the current value of each operation specified in <i>dwFlags</i>.

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

Until the mixer's video processor mode is set, the returned values are all zero. After the processor mode is set, the returned values reflect the current mode. To select a video processor mode, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode">IMFVideoProcessor::SetVideoProcessorMode</a>. Otherwise, the EVR automatically selects a mode when streaming begins.

To find out which ProcAmp settings the driver supports, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">IMFVideoProcessor::GetVideoProcessorCaps</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>