---
UID: NF:strmif.IAMTimecodeDisplay.SetTCDisplayEnable
title: IAMTimecodeDisplay::SetTCDisplayEnable (strmif.h)
description: The SetTCDisplayEnable method enables or disables an external device's timecode character output generator.
helpviewer_keywords: ["IAMTimecodeDisplay interface [DirectShow]","SetTCDisplayEnable method","IAMTimecodeDisplay.SetTCDisplayEnable","IAMTimecodeDisplay::SetTCDisplayEnable","IAMTimecodeDisplaySetTCDisplayEnable","SetTCDisplayEnable","SetTCDisplayEnable method [DirectShow]","SetTCDisplayEnable method [DirectShow]","IAMTimecodeDisplay interface","dshow.iamtimecodedisplay_settcdisplayenable","strmif/IAMTimecodeDisplay::SetTCDisplayEnable"]
old-location: dshow\iamtimecodedisplay_settcdisplayenable.htm
tech.root: dshow
ms.assetid: ae4eeeaa-1c73-4e3a-82b1-a073d9c7d667
ms.date: 4/26/2023
ms.keywords: IAMTimecodeDisplay interface [DirectShow],SetTCDisplayEnable method, IAMTimecodeDisplay.SetTCDisplayEnable, IAMTimecodeDisplay::SetTCDisplayEnable, IAMTimecodeDisplaySetTCDisplayEnable, SetTCDisplayEnable, SetTCDisplayEnable method [DirectShow], SetTCDisplayEnable method [DirectShow],IAMTimecodeDisplay interface, dshow.iamtimecodedisplay_settcdisplayenable, strmif/IAMTimecodeDisplay::SetTCDisplayEnable
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
 - IAMTimecodeDisplay::SetTCDisplayEnable
 - strmif/IAMTimecodeDisplay::SetTCDisplayEnable
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
 - IAMTimecodeDisplay.SetTCDisplayEnable
---

# IAMTimecodeDisplay::SetTCDisplayEnable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetTCDisplayEnable</code> method enables or disables an external device's timecode character output generator.

## -parameters

### -param State [in]

Value specifying whether to enable or disable the timecode character output generator. Specify OATRUE to enable or OAFALSE to disable.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

This method is not intended for rendering characters inside a filter graph, it is purely intended for hardware displays. Ensure that your external timecode reader or generator has display capability before trying to use this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodedisplay">IAMTimecodeDisplay Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodedisplay-gettcdisplayenable">IAMTimecodeDisplay::GetTCDisplayEnable</a>