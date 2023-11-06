---
UID: NN:strmif.IDDrawExclModeVideoCallback
title: IDDrawExclModeVideoCallback (strmif.h)
description: The IDDrawExclModeVideoCallback interface is a callback interface for the IDDrawExclModeVideo interface.This callback interface enables applications to get synchronous notification about changes to the overlay position, size, visibility, and so on, so that the application can adjust its video visibility, size, and position. This avoids any color key flash at the beginning, end, or during playback. The application must implement the interface. It is important that none of the methods block or slow down the video processing, because this will cause problems with playback.Use this interface if you are writing a filter that supports IDDrawExclModeVideo or needs to generate callbacks to enable an application to draw color keys at the right time.
helpviewer_keywords: ["IDDrawExclModeVideoCallback","IDDrawExclModeVideoCallback interface [DirectShow]","IDDrawExclModeVideoCallback interface [DirectShow]","described","IDDrawExclModeVideoCallbackInterface","dshow.iddrawexclmodevideocallback","strmif/IDDrawExclModeVideoCallback"]
old-location: dshow\iddrawexclmodevideocallback.htm
tech.root: dshow
ms.assetid: 7f22d4cd-93e0-4d7d-b8f3-932488d2c672
ms.date: 4/26/2023
ms.keywords: IDDrawExclModeVideoCallback, IDDrawExclModeVideoCallback interface [DirectShow], IDDrawExclModeVideoCallback interface [DirectShow],described, IDDrawExclModeVideoCallbackInterface, dshow.iddrawexclmodevideocallback, strmif/IDDrawExclModeVideoCallback
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
 - IDDrawExclModeVideoCallback
 - strmif/IDDrawExclModeVideoCallback
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
 - IDDrawExclModeVideoCallback
---

# IDDrawExclModeVideoCallback interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDDrawExclModeVideoCallback</code> interface is a callback interface for the <a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo</a> interface.

This callback interface enables applications to get synchronous notification about changes to the overlay position, size, visibility, and so on, so that the application can adjust its video visibility, size, and position. This avoids any color key flash at the beginning, end, or during playback. The application must implement the interface. It is important that none of the methods block or slow down the video processing, because this will cause problems with playback.

Use this interface if you are writing a filter that supports <b>IDDrawExclModeVideo</b> or needs to generate callbacks to enable an application to draw color keys at the right time.

## -inheritance

The <b>IDDrawExclModeVideoCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDDrawExclModeVideoCallback</b> also has these types of members:

