---
UID: NF:strmif.IAMAudioRendererStats.GetStatParam
title: IAMAudioRendererStats::GetStatParam (strmif.h)
description: The GetStatParam method retrieves performance information from the audio renderer.
helpviewer_keywords: ["GetStatParam","GetStatParam method [DirectShow]","GetStatParam method [DirectShow]","IAMAudioRendererStats interface","IAMAudioRendererStats interface [DirectShow]","GetStatParam method","IAMAudioRendererStats.GetStatParam","IAMAudioRendererStats::GetStatParam","IAMAudioRendererStatsGetStatParam","dshow.iamaudiorendererstats_getstatparam","strmif/IAMAudioRendererStats::GetStatParam"]
old-location: dshow\iamaudiorendererstats_getstatparam.htm
tech.root: dshow
ms.assetid: bc01cac7-316f-4d18-ae68-c3db4dbf03fa
ms.date: 4/26/2023
ms.keywords: GetStatParam, GetStatParam method [DirectShow], GetStatParam method [DirectShow],IAMAudioRendererStats interface, IAMAudioRendererStats interface [DirectShow],GetStatParam method, IAMAudioRendererStats.GetStatParam, IAMAudioRendererStats::GetStatParam, IAMAudioRendererStatsGetStatParam, dshow.iamaudiorendererstats_getstatparam, strmif/IAMAudioRendererStats::GetStatParam
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMAudioRendererStats::GetStatParam
 - strmif/IAMAudioRendererStats::GetStatParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAudioRendererStats.GetStatParam
---

# IAMAudioRendererStats::GetStatParam


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetStatParam</code> method retrieves performance information from the audio renderer.

## -parameters

### -param dwParam [in]

Specifies a member of the <a href="/windows/desktop/api/strmif/ne-strmif-_am_audio_renderer_stat_param">_AM_AUDIO_RENDERER_STAT_PARAM</a> enumeration, indicating which information to retrieve.

### -param pdwParam1 [out]

Pointer to a variable that receives performance information. The meaning of the returned value depends on the value of <i>dwParam</i>.

### -param pdwParam2 [out]

Pointer to a variable that receives performance information. The meaning of the returned value depends on the value of <i>dwParam</i>.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The renderer does not track the specified information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamaudiorendererstats">IAMAudioRendererStats Interface</a>