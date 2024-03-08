---
UID: NN:vpnotify.IVPBaseNotify
title: IVPBaseNotify (vpnotify.h)
description: Enables the Overlay Mixer to control the properties of a hardware device such as a decoder that uses a video port. The IVPNotify interface derives from this interface.Applications should never use this interface.
helpviewer_keywords: ["IVPBaseNotify","IVPBaseNotify interface [DirectShow]","IVPBaseNotify interface [DirectShow]","described","IVPBaseNotifyInterface","dshow.ivpbasenotify","vpnotify/IVPBaseNotify"]
old-location: dshow\ivpbasenotify.htm
tech.root: dshow
ms.assetid: c72bd662-366c-4102-9ad9-9e4c59096ede
ms.date: 4/26/2023
ms.keywords: IVPBaseNotify, IVPBaseNotify interface [DirectShow], IVPBaseNotify interface [DirectShow],described, IVPBaseNotifyInterface, dshow.ivpbasenotify, vpnotify/IVPBaseNotify
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
 - IVPBaseNotify
 - vpnotify/IVPBaseNotify
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
 - IVPBaseNotify
---

# IVPBaseNotify interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Enables the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> to control the properties of a hardware device such as a decoder that uses a video port. The <a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a> interface derives from this interface.

Applications should never use this interface.

## -inheritance

The <b>IVPBaseNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVPBaseNotify</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include Vptype.h before Vpnotify.h.

## -see-also

<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig</a>
