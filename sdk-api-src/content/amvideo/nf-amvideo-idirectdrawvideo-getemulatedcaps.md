---
UID: NF:amvideo.IDirectDrawVideo.GetEmulatedCaps
title: IDirectDrawVideo::GetEmulatedCaps (amvideo.h)
description: The GetEmulatedCaps method retrieves a DirectDraw-defined DDCAPS structure containing the emulated capabilities.
helpviewer_keywords: ["GetEmulatedCaps","GetEmulatedCaps method [DirectShow]","GetEmulatedCaps method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","GetEmulatedCaps method","IDirectDrawVideo.GetEmulatedCaps","IDirectDrawVideo::GetEmulatedCaps","IDirectDrawVideoGetEmulatedCaps","amvideo/IDirectDrawVideo::GetEmulatedCaps","dshow.idirectdrawvideo_getemulatedcaps"]
old-location: dshow\idirectdrawvideo_getemulatedcaps.htm
tech.root: dshow
ms.assetid: 623cd000-6194-458d-8ef1-5eca202756c1
ms.date: 4/26/2023
ms.keywords: GetEmulatedCaps, GetEmulatedCaps method [DirectShow], GetEmulatedCaps method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetEmulatedCaps method, IDirectDrawVideo.GetEmulatedCaps, IDirectDrawVideo::GetEmulatedCaps, IDirectDrawVideoGetEmulatedCaps, amvideo/IDirectDrawVideo::GetEmulatedCaps, dshow.idirectdrawvideo_getemulatedcaps
req.header: amvideo.h
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
 - IDirectDrawVideo::GetEmulatedCaps
 - amvideo/IDirectDrawVideo::GetEmulatedCaps
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
 - IDirectDrawVideo.GetEmulatedCaps
---

# IDirectDrawVideo::GetEmulatedCaps


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetEmulatedCaps</code> method retrieves a DirectDraw-defined DDCAPS structure containing the emulated capabilities.

## -parameters

### -param pCaps

Pointer to a <b>DDCAPS</b> structure containing the emulated capabilities.

## -returns

Returns an <b>HRESULT</b> value. If the renderer has not loaded DirectDraw, this method returns E_FAIL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>