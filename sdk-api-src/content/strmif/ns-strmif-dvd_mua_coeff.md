---
UID: NS:strmif.tagDVD_MUA_Coeff
title: DVD_MUA_Coeff (strmif.h)
description: The DVD_MUA_Coeff structure defines the mixing coefficients for one channel in a multichannel audio stream. The DVD_MultichannelAudioAttributes structure contains an array of eight DVD_MUA_Coeff structures, one for each channel in the stream.
helpviewer_keywords: ["DVD_MUA_Coeff","DVD_MUA_Coeff structure [DirectShow]","DVD_MUA_CoeffStructure","dshow.dvd_mua_coeff","strmif/DVD_MUA_Coeff"]
old-location: dshow\dvd_mua_coeff.htm
tech.root: dshow
ms.assetid: 8b8402da-37c2-4983-ae09-967c269fc828
ms.date: 4/26/2023
ms.keywords: DVD_MUA_Coeff, DVD_MUA_Coeff structure [DirectShow], DVD_MUA_CoeffStructure, dshow.dvd_mua_coeff, strmif/DVD_MUA_Coeff
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DVD_MUA_Coeff
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_MUA_Coeff
 - strmif/tagDVD_MUA_Coeff
 - DVD_MUA_Coeff
 - strmif/DVD_MUA_Coeff
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_MUA_Coeff
---

# DVD_MUA_Coeff structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The [DVD_MultichannelAudioAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_multichannelaudioattributes) structure contains an array of eight <code>DVD_MUA_Coeff</code> structures, one for each channel in the stream.

## -struct-fields

### -field log2_alpha

The mixing coefficient for this channel to channel 0.

### -field log2_beta

The mixing coefficient for this channel to channel 1.

## -remarks

The information contained in this structure reflects the mixing coefficients as authored on the digital video disc (DVD). An application cannot modify these values or otherwise use them unless it is also decoding the audio. In the typical DVD filter graph, the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter does not send this information to the decoder.

The alpha coefficient is used to mix to audio channel 0 and the beta coefficient is used to mix to audio channel 1. In general, the following formula calculates the mixing coefficients.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
Audio channel 0 = coeff[0].alpha * value[0] + coeff[1].alpha * value[1] + ... 
Audio channel 1 = coeff[0].beta * value[0]  + coeff[1].beta * value[1] + ... 
</pre>
</td>
</tr>
</table></span></div>

## -see-also

[DVD_AudioAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_audioattributes)



[DVD_MUA_MixingInfo](/windows/desktop/api/strmif/ns-strmif-dvd_mua_mixinginfo)



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>