---
UID: NF:strmif.IAMVideoControl.GetCurrentActualFrameRate
title: IAMVideoControl::GetCurrentActualFrameRate (strmif.h)
description: The GetCurrentActualFrameRate method retrieves the actual frame rate, expressed as a frame duration in 100-nanosecond units.
helpviewer_keywords: ["GetCurrentActualFrameRate","GetCurrentActualFrameRate method [DirectShow]","GetCurrentActualFrameRate method [DirectShow]","IAMVideoControl interface","IAMVideoControl interface [DirectShow]","GetCurrentActualFrameRate method","IAMVideoControl.GetCurrentActualFrameRate","IAMVideoControl::GetCurrentActualFrameRate","IAMVideoControlGetCurrentActualFrameRate","dshow.iamvideocontrol_getcurrentactualframerate","strmif/IAMVideoControl::GetCurrentActualFrameRate"]
old-location: dshow\iamvideocontrol_getcurrentactualframerate.htm
tech.root: dshow
ms.assetid: 373cabed-af09-4d54-b4e1-0ef87727430a
ms.date: 4/26/2023
ms.keywords: GetCurrentActualFrameRate, GetCurrentActualFrameRate method [DirectShow], GetCurrentActualFrameRate method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetCurrentActualFrameRate method, IAMVideoControl.GetCurrentActualFrameRate, IAMVideoControl::GetCurrentActualFrameRate, IAMVideoControlGetCurrentActualFrameRate, dshow.iamvideocontrol_getcurrentactualframerate, strmif/IAMVideoControl::GetCurrentActualFrameRate
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
 - IAMVideoControl::GetCurrentActualFrameRate
 - strmif/IAMVideoControl::GetCurrentActualFrameRate
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
 - IAMVideoControl.GetCurrentActualFrameRate
---

# IAMVideoControl::GetCurrentActualFrameRate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentActualFrameRate</code> method retrieves the actual frame rate, expressed as a frame duration in 100-nanosecond units. USB (Universal Serial Bus) and IEEE 1394 cameras may provide lower frame rates than requested because of bandwidth availability. This is only available during video streaming.

## -parameters

### -param pPin [in]

Pointer to the pin to retrieve the frame rate from.

### -param ActualFrameRate [out]

Pointer to the frame rate in frame duration in 100-nanosecond units.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl Interface</a>