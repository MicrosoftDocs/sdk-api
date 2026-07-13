---
UID: NF:strmif.IAMTuner.SignalPresent
title: IAMTuner::SignalPresent (strmif.h)
description: The SignalPresent method retrieves the strength of the signal on a given channel.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","SignalPresent method","IAMTuner.SignalPresent","IAMTuner::SignalPresent","IAMTunerSignalPresent","SignalPresent","SignalPresent method [DirectShow]","SignalPresent method [DirectShow]","IAMTuner interface","dshow.iamtuner_signalpresent","strmif/IAMTuner::SignalPresent"]
old-location: dshow\iamtuner_signalpresent.htm
tech.root: dshow
ms.assetid: 64a89038-4df1-4e30-8952-6dc039a2e18b
ms.date: 4/26/2023
ms.keywords: IAMTuner interface [DirectShow],SignalPresent method, IAMTuner.SignalPresent, IAMTuner::SignalPresent, IAMTunerSignalPresent, SignalPresent, SignalPresent method [DirectShow], SignalPresent method [DirectShow],IAMTuner interface, dshow.iamtuner_signalpresent, strmif/IAMTuner::SignalPresent
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
 - IAMTuner::SignalPresent
 - strmif/IAMTuner::SignalPresent
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
 - IAMTuner.SignalPresent
---

# IAMTuner::SignalPresent


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SignalPresent</code> method retrieves the strength of the signal on a given channel.

## -parameters

### -param plSignalStrength [out]

Pointer to a variable that receives a value indicating whether a signal is present on the current channel. Can be one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AMTUNER_HASNOSIGNALSTRENGTH</td>
<td>-1</td>
</tr>
<tr>
<td>AMTUNER_NOSIGNAL</td>
<td>0</td>
</tr>
<tr>
<td>AMTUNER_SIGNALPRESENT</td>
<td>1</td>
</tr>
</table>
 

A value of AMTUNER_HASNOSIGNALSTRENGTH means the signal strength cannot be determined at this time.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>