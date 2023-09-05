---
UID: NF:strmif.IAMTVTuner.AutoTune
title: IAMTVTuner::AutoTune (strmif.h)
description: The AutoTune method scans for a precise signal on the channel's frequency.
helpviewer_keywords: ["AutoTune","AutoTune method [DirectShow]","AutoTune method [DirectShow]","IAMTVTuner interface","IAMTVTuner interface [DirectShow]","AutoTune method","IAMTVTuner.AutoTune","IAMTVTuner::AutoTune","IAMTVTunerAutoTune","dshow.iamtvtuner_autotune","strmif/IAMTVTuner::AutoTune"]
old-location: dshow\iamtvtuner_autotune.htm
tech.root: dshow
ms.assetid: ae8338e4-b75d-42d5-bcb7-84352921458c
ms.date: 4/26/2023
ms.keywords: AutoTune, AutoTune method [DirectShow], AutoTune method [DirectShow],IAMTVTuner interface, IAMTVTuner interface [DirectShow],AutoTune method, IAMTVTuner.AutoTune, IAMTVTuner::AutoTune, IAMTVTunerAutoTune, dshow.iamtvtuner_autotune, strmif/IAMTVTuner::AutoTune
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
 - IAMTVTuner::AutoTune
 - strmif/IAMTVTuner::AutoTune
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
 - IAMTVTuner.AutoTune
---

# IAMTVTuner::AutoTune


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AutoTune</code> method scans for a precise signal on the channel's frequency.

## -parameters

### -param lChannel [in]

TV channel number.

### -param plFoundSignal [out]

Pointer to a variable indicating whether the channel's frequency was found; nonzero indicates found, zero indicates not found.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

TV channels generally map to a unique frequency depending on regional variances. To avoid interference between multiple transmitters that are assigned the same channel when they are in close geographic proximity, small frequency offsets are introduced at each transmitter. In the United States, this offset ranges up to +/– 26.25 kilohertz (kHz).

This method handles the channel-to-frequency conversion and scans for the most precise frequency. Store these values by calling the <a href="/windows/desktop/api/strmif/nf-strmif-iamtvtuner-storeautotune">IAMTVTuner::StoreAutoTune</a> method. You can find base frequencies for channels in the appendix <a href="/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>