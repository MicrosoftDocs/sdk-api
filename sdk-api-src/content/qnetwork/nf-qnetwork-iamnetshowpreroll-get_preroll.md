---
UID: NF:qnetwork.IAMNetShowPreroll.get_Preroll
title: IAMNetShowPreroll::get_Preroll (qnetwork.h)
description: The get_Preroll method queries whether the filter is currently prerolling.
helpviewer_keywords: ["IAMNetShowPreroll interface [DirectShow]","get_Preroll method","IAMNetShowPreroll.get_Preroll","IAMNetShowPreroll::get_Preroll","IAMNetShowPrerollget_Preroll","dshow.iamnetshowpreroll_get_preroll","get_Preroll","get_Preroll method [DirectShow]","get_Preroll method [DirectShow]","IAMNetShowPreroll interface","qnetwork/IAMNetShowPreroll::get_Preroll"]
old-location: dshow\iamnetshowpreroll_get_preroll.htm
tech.root: dshow
ms.assetid: c868a997-9d22-452b-9d57-6bd34b054d35
ms.date: 4/26/2023
ms.keywords: IAMNetShowPreroll interface [DirectShow],get_Preroll method, IAMNetShowPreroll.get_Preroll, IAMNetShowPreroll::get_Preroll, IAMNetShowPrerollget_Preroll, dshow.iamnetshowpreroll_get_preroll, get_Preroll, get_Preroll method [DirectShow], get_Preroll method [DirectShow],IAMNetShowPreroll interface, qnetwork/IAMNetShowPreroll::get_Preroll
req.header: qnetwork.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMNetShowPreroll::get_Preroll
 - qnetwork/IAMNetShowPreroll::get_Preroll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowPreroll.get_Preroll
---

# IAMNetShowPreroll::get_Preroll


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Preroll</code> method queries whether the filter is currently prerolling.

## -parameters

### -param pfPreroll

Pointer to a variable that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowpreroll">IAMNetShowPreroll Interface</a>