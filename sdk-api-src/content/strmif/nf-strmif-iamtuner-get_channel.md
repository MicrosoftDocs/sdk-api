---
UID: NF:strmif.IAMTuner.get_Channel
title: IAMTuner::get_Channel (strmif.h)
description: The get_Channel method retrieves the channel to which the tuner is set.
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","get_Channel method","IAMTVTuner::get_Channel","IAMTuner interface [DirectShow]","get_Channel method","IAMTuner.get_Channel","IAMTuner::get_Channel","IAMTunerget_Channel","dshow.iamtuner_get_channel","get_Channel","get_Channel method [DirectShow]","get_Channel method [DirectShow]","IAMTVTuner interface","get_Channel method [DirectShow]","IAMTuner interface","strmif/IAMTVTuner::get_Channel","strmif/IAMTuner::get_Channel"]
old-location: dshow\iamtuner_get_channel.htm
tech.root: dshow
ms.assetid: 68c1b6da-4380-4831-b554-bbb2e3e55ef9
ms.date: 4/26/2023
ms.keywords: IAMTVTuner interface [DirectShow],get_Channel method, IAMTVTuner::get_Channel, IAMTuner interface [DirectShow],get_Channel method, IAMTuner.get_Channel, IAMTuner::get_Channel, IAMTunerget_Channel, dshow.iamtuner_get_channel, get_Channel, get_Channel method [DirectShow], get_Channel method [DirectShow],IAMTVTuner interface, get_Channel method [DirectShow],IAMTuner interface, strmif/IAMTVTuner::get_Channel, strmif/IAMTuner::get_Channel
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMTuner::get_Channel
 - strmif/IAMTuner::get_Channel
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
 - IAMTuner.get_Channel
 - IAMTVTuner.get_Channel
---

# IAMTuner::get_Channel


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Channel</code> method retrieves the channel to which the tuner is set.

## -parameters

### -param plChannel [out]

Pointer to a variable that receives the channel. For frequencies, see <a href="/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>

### -param plVideoSubChannel [out]

Pointer to a variable that receives either the video subchannel, or one of the following flags:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AMTUNER_SUBCHAN_DEFAULT</td>
<td>Default subchannel</td>
</tr>
<tr>
<td>AMTUNER_SUBCHAN_NO_TUNE</td>
<td>No subchannel tuning</td>
</tr>
</table>

### -param plAudioSubChannel [out]

Pointer to a variable that receives either the audio subchannel, or one of the following flags:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AMTUNER_SUBCHAN_DEFAULT</td>
<td>Default subchannel</td>
</tr>
<tr>
<td>AMTUNER_SUBCHAN_NO_TUNE</td>
<td>No subchannel tuning</td>
</tr>
</table>

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>