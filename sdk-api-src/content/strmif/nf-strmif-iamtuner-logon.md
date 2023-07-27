---
UID: NF:strmif.IAMTuner.Logon
title: IAMTuner::Logon (strmif.h)
description: The Logon method logs a user onto the system.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","Logon method","IAMTuner.Logon","IAMTuner::Logon","IAMTunerLogon","Logon","Logon method [DirectShow]","Logon method [DirectShow]","IAMTuner interface","dshow.iamtuner_logon","strmif/IAMTuner::Logon"]
old-location: dshow\iamtuner_logon.htm
tech.root: dshow
ms.assetid: b4a5a927-254c-44cd-b17d-e1f47b3f62a7
ms.date: 4/26/2023
ms.keywords: IAMTuner interface [DirectShow],Logon method, IAMTuner.Logon, IAMTuner::Logon, IAMTunerLogon, Logon, Logon method [DirectShow], Logon method [DirectShow],IAMTuner interface, dshow.iamtuner_logon, strmif/IAMTuner::Logon
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
 - IAMTuner::Logon
 - strmif/IAMTuner::Logon
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
 - IAMTuner.Logon
---

# IAMTuner::Logon


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Logon</code> method logs a user onto the system.

## -parameters

### -param hCurrentUser [in]

Handle to an application-defined data structure that identifies the current user.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The <code>Logon</code> and <b>Logout</b> methods enable you to implement selective user access.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>