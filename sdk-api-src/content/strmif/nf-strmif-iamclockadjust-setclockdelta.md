---
UID: NF:strmif.IAMClockAdjust.SetClockDelta
title: IAMClockAdjust::SetClockDelta (strmif.h)
description: The SetClockDelta method adjusts the clock time.
helpviewer_keywords: ["IAMClockAdjust interface [DirectShow]","SetClockDelta method","IAMClockAdjust.SetClockDelta","IAMClockAdjust::SetClockDelta","IAMClockAdjustSetClockDelta","SetClockDelta","SetClockDelta method [DirectShow]","SetClockDelta method [DirectShow]","IAMClockAdjust interface","dshow.iamclockadjust_setclockdelta","strmif/IAMClockAdjust::SetClockDelta"]
old-location: dshow\iamclockadjust_setclockdelta.htm
tech.root: dshow
ms.assetid: f9bd4e69-343f-4150-ab12-b5ce405a3ac3
ms.date: 4/26/2023
ms.keywords: IAMClockAdjust interface [DirectShow],SetClockDelta method, IAMClockAdjust.SetClockDelta, IAMClockAdjust::SetClockDelta, IAMClockAdjustSetClockDelta, SetClockDelta, SetClockDelta method [DirectShow], SetClockDelta method [DirectShow],IAMClockAdjust interface, dshow.iamclockadjust_setclockdelta, strmif/IAMClockAdjust::SetClockDelta
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
 - IAMClockAdjust::SetClockDelta
 - strmif/IAMClockAdjust::SetClockDelta
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
 - IAMClockAdjust.SetClockDelta
---

# IAMClockAdjust::SetClockDelta


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetClockDelta</code> method adjusts the clock time.

## -parameters

### -param rtDelta [in]

Specifies the amount by which to adjust the clock, as a <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> value. A positive value moves the clock forward, and a negative value moves the clock backward.

## -returns

Returns S_OK or an <b>HRESULT</b> error code.

## -remarks

The time values returned by <a href="/windows/desktop/api/strmif/nf-strmif-ireferenceclock-gettime">IReferenceClock::GetTime</a> are monotonically increasing. If you set the clock back, <b>GetTime</b> continues to report the old time until the internal clock catches up.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamclockadjust">IAMClockAdjust Interface</a>