---
UID: NF:strmif.IAMExtTransport.put_Rate
title: IAMExtTransport::put_Rate (strmif.h)
description: The put_Rate method sets the playback rate for variable-speed external devices.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","put_Rate method","IAMExtTransport.put_Rate","IAMExtTransport::put_Rate","IAMExtTransportput_Rate","dshow.iamexttransport_put_rate","put_Rate","put_Rate method [DirectShow]","put_Rate method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::put_Rate"]
old-location: dshow\iamexttransport_put_rate.htm
tech.root: dshow
ms.assetid: 165966f1-f826-4ce2-b520-4a420898eee4
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],put_Rate method, IAMExtTransport.put_Rate, IAMExtTransport::put_Rate, IAMExtTransportput_Rate, dshow.iamexttransport_put_rate, put_Rate, put_Rate method [DirectShow], put_Rate method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_Rate
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
 - IAMExtTransport::put_Rate
 - strmif/IAMExtTransport::put_Rate
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
 - IAMExtTransport.put_Rate
---

# IAMExtTransport::put_Rate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Rate</code> method sets the playback rate for variable-speed external devices.



This method is not implemented.

## -parameters

### -param dblRate [in]

Specifies the rate as a multiple of normal playback rate. For example, 0.5 specifies half speed, and 2.0 specifies double speed.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_rate">IAMExtTransport::get_Rate</a>