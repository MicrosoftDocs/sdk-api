---
UID: NF:strmif.IAMovieSetup.Register
title: IAMovieSetup::Register (strmif.h)
description: Note  The IAMovieSetup interface is deprecated. Use the AMovieDllRegisterServer2 function instead. Adds the filter to the registry.
helpviewer_keywords: ["IAMovieSetup interface [DirectShow]","Register method","IAMovieSetup.Register","IAMovieSetup::Register","IAMovieSetupRegister","Register","Register method [DirectShow]","Register method [DirectShow]","IAMovieSetup interface","dshow.iamoviesetup_register","strmif/IAMovieSetup::Register"]
old-location: dshow\iamoviesetup_register.htm
tech.root: dshow
ms.assetid: c39edba2-df48-43e4-9a0d-d5c409a8a9d0
ms.date: 4/26/2023
ms.keywords: IAMovieSetup interface [DirectShow],Register method, IAMovieSetup.Register, IAMovieSetup::Register, IAMovieSetupRegister, Register, Register method [DirectShow], Register method [DirectShow],IAMovieSetup interface, dshow.iamoviesetup_register, strmif/IAMovieSetup::Register
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMovieSetup::Register
 - strmif/IAMovieSetup::Register
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMovieSetup.Register
---

# IAMovieSetup::Register


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IAMovieSetup</b> interface is deprecated. Use the <a href="/windows/desktop/DirectShow/amoviedllregisterserver2">AMovieDllRegisterServer2</a> function instead.</div>
<div> </div>
Adds the filter to the registry.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method registers the filter, its pins, and the media type associated with the pins. It should be implemented to use <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper</a> methods to accomplish this. See the <a href="/windows/desktop/DirectShow/cbasefilter-register">CBaseFilter::Register</a> member function for a description of its implementation.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamoviesetup">IAMovieSetup Interface</a>
