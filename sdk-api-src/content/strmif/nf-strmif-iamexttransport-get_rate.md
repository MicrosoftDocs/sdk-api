---
UID: NF:strmif.IAMExtTransport.get_Rate
title: IAMExtTransport::get_Rate (strmif.h)
description: The get_Rate method retrieves the playback rate for variable-speed external devices.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","get_Rate method","IAMExtTransport.get_Rate","IAMExtTransport::get_Rate","IAMExtTransportget_Rate","dshow.iamexttransport_get_rate","get_Rate","get_Rate method [DirectShow]","get_Rate method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::get_Rate"]
old-location: dshow\iamexttransport_get_rate.htm
tech.root: dshow
ms.assetid: 35a2fb2b-0963-4bdb-86a4-b5950b48a834
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],get_Rate method, IAMExtTransport.get_Rate, IAMExtTransport::get_Rate, IAMExtTransportget_Rate, dshow.iamexttransport_get_rate, get_Rate, get_Rate method [DirectShow], get_Rate method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_Rate
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
 - IAMExtTransport::get_Rate
 - strmif/IAMExtTransport::get_Rate
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
 - IAMExtTransport.get_Rate
---

# IAMExtTransport::get_Rate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Rate</code> method retrieves the playback rate for variable-speed external devices.



This method is not implemented.

## -parameters

### -param pdblRate [out]

Pointer to a <b>double</b> to receive the playback rate that was set using <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_rate">IAMExtTransport::put_Rate</a>.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>