---
UID: NF:strmif.IIPDVDec.get_IPDisplay
title: IIPDVDec::get_IPDisplay (strmif.h)
description: The get_IPDisplay method gets the decoding resolution.
helpviewer_keywords: ["IIPDVDec interface [DirectShow]","get_IPDisplay method","IIPDVDec.get_IPDisplay","IIPDVDec::get_IPDisplay","IIPDVDecget_IPDisplay","dshow.iipdvdec_get_ipdisplay","get_IPDisplay","get_IPDisplay method [DirectShow]","get_IPDisplay method [DirectShow]","IIPDVDec interface","strmif/IIPDVDec::get_IPDisplay"]
old-location: dshow\iipdvdec_get_ipdisplay.htm
tech.root: dshow
ms.assetid: 9bf8e318-48b7-4aa8-a8c5-974b320f31ce
ms.date: 4/26/2023
ms.keywords: IIPDVDec interface [DirectShow],get_IPDisplay method, IIPDVDec.get_IPDisplay, IIPDVDec::get_IPDisplay, IIPDVDecget_IPDisplay, dshow.iipdvdec_get_ipdisplay, get_IPDisplay, get_IPDisplay method [DirectShow], get_IPDisplay method [DirectShow],IIPDVDec interface, strmif/IIPDVDec::get_IPDisplay
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
 - IIPDVDec::get_IPDisplay
 - strmif/IIPDVDec::get_IPDisplay
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
 - IIPDVDec.get_IPDisplay
---

# IIPDVDec::get_IPDisplay


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_IPDisplay</code> method gets the decoding resolution.

## -parameters

### -param displayPix

Receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-_dvresolution">DVDECODERRESOLUTION</a> enumerated type, specifying the decoding resolution.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iipdvdec">IIPDVDec Interface</a>