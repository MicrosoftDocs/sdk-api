---
UID: NN:strmif.IAMovieSetup
title: IAMovieSetup (strmif.h)
description: Note  This interface has been deprecated. (IAMovieSetup)
helpviewer_keywords: ["IAMovieSetup","IAMovieSetup interface [DirectShow]","IAMovieSetup interface [DirectShow]","described","IAMovieSetupInterface","dshow.iamoviesetup","strmif/IAMovieSetup"]
old-location: dshow\iamoviesetup.htm
tech.root: dshow
ms.assetid: b200dbee-bab7-43d7-a204-751592fa2405
ms.date: 4/26/2023
ms.keywords: IAMovieSetup, IAMovieSetup interface [DirectShow], IAMovieSetup interface [DirectShow],described, IAMovieSetupInterface, dshow.iamoviesetup, strmif/IAMovieSetup
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAMovieSetup
 - strmif/IAMovieSetup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMovieSetup
---

# IAMovieSetup interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated. It is used by two obsolete functions, <a href="/windows/desktop/DirectShow/amoviedllregisterserver">AMovieDllRegisterServer</a> and <a href="/windows/desktop/DirectShow/amoviedllunregisterserver">AMovieDllUnregisterServer</a>. These functions are now replaced by <a href="/windows/desktop/DirectShow/amoviedllregisterserver2">AMovieDllRegisterServer2</a>, which does not require <b>IAMovieSetup</b>. However, <b>IAMovieSetup</b> will continue to be supported for backward compatibility with existing applications.</div>
<div> </div>

## -inheritance

The <b>IAMovieSetup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMovieSetup</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
