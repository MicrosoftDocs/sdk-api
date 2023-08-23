---
UID: NF:strmif.IAMVideoProcAmp.Get
title: IAMVideoProcAmp::Get (strmif.h)
description: The Get method gets the current setting of a video property.
helpviewer_keywords: ["Get","Get method [DirectShow]","Get method [DirectShow]","IAMVideoProcAmp interface","IAMVideoProcAmp interface [DirectShow]","Get method","IAMVideoProcAmp.Get","IAMVideoProcAmp::Get","IAMVideoProcAmpGet","dshow.iamvideoprocamp_get","strmif/IAMVideoProcAmp::Get"]
old-location: dshow\iamvideoprocamp_get.htm
tech.root: dshow
ms.assetid: 8924383e-23e1-4732-9eff-dc7c8d0e361a
ms.date: 4/26/2023
ms.keywords: Get, Get method [DirectShow], Get method [DirectShow],IAMVideoProcAmp interface, IAMVideoProcAmp interface [DirectShow],Get method, IAMVideoProcAmp.Get, IAMVideoProcAmp::Get, IAMVideoProcAmpGet, dshow.iamvideoprocamp_get, strmif/IAMVideoProcAmp::Get
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
 - IAMVideoProcAmp::Get
 - strmif/IAMVideoProcAmp::Get
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
 - IAMVideoProcAmp.Get
---

# IAMVideoProcAmp::Get


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Get</code> method gets the current setting of a video property.

## -parameters

### -param Property [in]

Specifies the property to retrieve, as a value from the [VideoProcAmpProperty](/windows/desktop/api/strmif/ne-strmif-videoprocampproperty) enumeration.

### -param lValue [out]

Receives the value of the property.

### -param Flags [out]

Receives a member of the [VideoProcAmpFlags](/windows/desktop/api/strmif/ne-strmif-videoprocampflags) enumeration. The returned value indicates whether the setting is controlled manually or automatically.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamvideoprocamp-set">IAMVideoProcAmp::Set</a>