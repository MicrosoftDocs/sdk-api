---
UID: NF:strmif.IAMTuner.put_Channel
title: IAMTuner::put_Channel (strmif.h)
description: The put_Channel method sets the TV channel.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","put_Channel method","IAMTuner.put_Channel","IAMTuner::put_Channel","IAMTunerput_Channel","dshow.iamtuner_put_channel","put_Channel","put_Channel method [DirectShow]","put_Channel method [DirectShow]","IAMTuner interface","strmif/IAMTuner::put_Channel"]
old-location: dshow\iamtuner_put_channel.htm
tech.root: dshow
ms.assetid: 47ad4288-d855-41cd-b8a2-7b3733a87b41
ms.date: 4/26/2023
ms.keywords: IAMTuner interface [DirectShow],put_Channel method, IAMTuner.put_Channel, IAMTuner::put_Channel, IAMTunerput_Channel, dshow.iamtuner_put_channel, put_Channel, put_Channel method [DirectShow], put_Channel method [DirectShow],IAMTuner interface, strmif/IAMTuner::put_Channel
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
 - IAMTuner::put_Channel
 - strmif/IAMTuner::put_Channel
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
 - IAMTuner.put_Channel
---

# IAMTuner::put_Channel


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Channel</code> method sets the TV channel.

## -parameters

### -param lChannel [in]

TV channel number.

### -param lVideoSubChannel

Predefined video subchannel value. Specify AMTUNER_SUBCHAN_NO_TUNE for no tuning or AMTUNER_SUBCHAN_DEFAULT for default subchannel. Meaningful only for satellite broadcasts.

### -param lAudioSubChannel

Predefined audio subchannel value. Specify AMTUNER_SUBCHAN_NO_TUNE for no tuning or AMTUNER_SUBCHAN_DEFAULT for default subchannel. Meaningful only for satellite broadcasts.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

This method handles the channel-to-frequency function call that converts the TV channel to a TV frequency. For a list of frequencies for channels, see <a href="/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>