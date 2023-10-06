---
UID: NF:vpnotify.IVPBaseNotify.RenegotiateVPParameters
title: IVPBaseNotify::RenegotiateVPParameters (vpnotify.h)
description: The RenegotiateVPParameters method initializes the connection to the decoder.
helpviewer_keywords: ["IVPBaseNotify interface [DirectShow]","RenegotiateVPParameters method","IVPBaseNotify.RenegotiateVPParameters","IVPBaseNotify::RenegotiateVPParameters","IVPBaseNotifyRenegotiateVPParameters","RenegotiateVPParameters","RenegotiateVPParameters method [DirectShow]","RenegotiateVPParameters method [DirectShow]","IVPBaseNotify interface","dshow.ivpbasenotify_renegotiatevpparameters","vpnotify/IVPBaseNotify::RenegotiateVPParameters"]
old-location: dshow\ivpbasenotify_renegotiatevpparameters.htm
tech.root: dshow
ms.assetid: b35a0e8f-3d4f-443d-b76c-83b44745a86d
ms.date: 4/26/2023
ms.keywords: IVPBaseNotify interface [DirectShow],RenegotiateVPParameters method, IVPBaseNotify.RenegotiateVPParameters, IVPBaseNotify::RenegotiateVPParameters, IVPBaseNotifyRenegotiateVPParameters, RenegotiateVPParameters, RenegotiateVPParameters method [DirectShow], RenegotiateVPParameters method [DirectShow],IVPBaseNotify interface, dshow.ivpbasenotify_renegotiatevpparameters, vpnotify/IVPBaseNotify::RenegotiateVPParameters
req.header: vpnotify.h
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
 - IVPBaseNotify::RenegotiateVPParameters
 - vpnotify/IVPBaseNotify::RenegotiateVPParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpnotify.h
api_name:
 - IVPBaseNotify.RenegotiateVPParameters
---

# IVPBaseNotify::RenegotiateVPParameters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RenegotiateVPParameters</code> method initializes the connection to the decoder.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter negotiates various parameters (by using the <a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig</a> interface) with the decoder or driver. Call this method if any of those parameters (such as the video format or size) change. Currently, the Overlay Mixer repeats the whole connection process. You can call this method even while the graph is playing.

Include Vptype.h before Vpnotify.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpbasenotify">IVPBaseNotify Interface</a>
