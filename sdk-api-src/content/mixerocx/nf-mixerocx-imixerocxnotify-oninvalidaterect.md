---
UID: NF:mixerocx.IMixerOCXNotify.OnInvalidateRect
title: IMixerOCXNotify::OnInvalidateRect (mixerocx.h)
description: The OnInvalidateRect method notifies the client that the video rectangle has been invalidated.
helpviewer_keywords: ["IMixerOCXNotify interface [DirectShow]","OnInvalidateRect method","IMixerOCXNotify.OnInvalidateRect","IMixerOCXNotify::OnInvalidateRect","IMixerOCXNotifyOnInvalidateRect","OnInvalidateRect","OnInvalidateRect method [DirectShow]","OnInvalidateRect method [DirectShow]","IMixerOCXNotify interface","dshow.imixerocxnotify_oninvalidaterect","mixerocx/IMixerOCXNotify::OnInvalidateRect"]
old-location: dshow\imixerocxnotify_oninvalidaterect.htm
tech.root: dshow
ms.assetid: 55d349d4-1a9a-4762-8058-c3f7a559e272
ms.date: 4/26/2023
ms.keywords: IMixerOCXNotify interface [DirectShow],OnInvalidateRect method, IMixerOCXNotify.OnInvalidateRect, IMixerOCXNotify::OnInvalidateRect, IMixerOCXNotifyOnInvalidateRect, OnInvalidateRect, OnInvalidateRect method [DirectShow], OnInvalidateRect method [DirectShow],IMixerOCXNotify interface, dshow.imixerocxnotify_oninvalidaterect, mixerocx/IMixerOCXNotify::OnInvalidateRect
req.header: mixerocx.h
req.include-header: 
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
 - IMixerOCXNotify::OnInvalidateRect
 - mixerocx/IMixerOCXNotify::OnInvalidateRect
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
 - IMixerOCXNotify.OnInvalidateRect
---

# IMixerOCXNotify::OnInvalidateRect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>OnInvalidateRect</code> method notifies the client that the video rectangle has been invalidated.

## -parameters

### -param lpcRect [in]

Specifies the rectangle that has been invalidated, in screen coordinates.

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify">IMixerOCXNotify Interface</a>