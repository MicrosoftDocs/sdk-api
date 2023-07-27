---
UID: NF:strmif.IDDrawExclModeVideoCallback.OnUpdateSize
title: IDDrawExclModeVideoCallback::OnUpdateSize (strmif.h)
description: The OnUpdateSize method informs the application that the size of the video rectangle is about to change.
helpviewer_keywords: ["IDDrawExclModeVideoCallback interface [DirectShow]","OnUpdateSize method","IDDrawExclModeVideoCallback.OnUpdateSize","IDDrawExclModeVideoCallback::OnUpdateSize","IDDrawExclModeVideoCallbackOnUpdateSize","OnUpdateSize","OnUpdateSize method [DirectShow]","OnUpdateSize method [DirectShow]","IDDrawExclModeVideoCallback interface","dshow.iddrawexclmodevideocallback_onupdatesize","strmif/IDDrawExclModeVideoCallback::OnUpdateSize"]
old-location: dshow\iddrawexclmodevideocallback_onupdatesize.htm
tech.root: dshow
ms.assetid: 00ddf110-8efc-414f-abfa-d6c7a22751a8
ms.date: 4/26/2023
ms.keywords: IDDrawExclModeVideoCallback interface [DirectShow],OnUpdateSize method, IDDrawExclModeVideoCallback.OnUpdateSize, IDDrawExclModeVideoCallback::OnUpdateSize, IDDrawExclModeVideoCallbackOnUpdateSize, OnUpdateSize, OnUpdateSize method [DirectShow], OnUpdateSize method [DirectShow],IDDrawExclModeVideoCallback interface, dshow.iddrawexclmodevideocallback_onupdatesize, strmif/IDDrawExclModeVideoCallback::OnUpdateSize
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
 - IDDrawExclModeVideoCallback::OnUpdateSize
 - strmif/IDDrawExclModeVideoCallback::OnUpdateSize
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
 - IDDrawExclModeVideoCallback.OnUpdateSize
---

# IDDrawExclModeVideoCallback::OnUpdateSize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>OnUpdateSize</code> method informs the application that the size of the video rectangle is about to change.

## -parameters

### -param dwWidth [in]

The new width, in pixels, of the video stream.

### -param dwHeight [in]

The new height, in pixels, of the video stream.

### -param dwARWidth [in]

The new horizontal value of the aspect ratio.

### -param dwARHeight [in]

The new vertical value of the aspect ratio.

## -returns

Returns an HRESULT value.

## -remarks

This method is called when the size of the rectangle in the video stream changes, for example from 704x480 to 640x480.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideocallback">IDDrawExclModeVideoCallback Interface</a>