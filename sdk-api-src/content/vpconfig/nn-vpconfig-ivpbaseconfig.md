---
UID: NN:vpconfig.IVPBaseConfig
title: IVPBaseConfig (vpconfig.h)
description: IVPBaseConfig is implemented on a filter that wraps a hardware device such as a decoder or capture device, if the device has a video port to the graphics adapter.
helpviewer_keywords: ["IVPBaseConfig","IVPBaseConfig interface [DirectShow]","IVPBaseConfig interface [DirectShow]","described","IVPBaseConfigInterface","dshow.ivpbaseconfig","vpconfig/IVPBaseConfig"]
old-location: dshow\ivpbaseconfig.htm
tech.root: dshow
ms.assetid: d9a4f395-3d2f-429a-884d-90131927a929
ms.date: 4/26/2023
ms.keywords: IVPBaseConfig, IVPBaseConfig interface [DirectShow], IVPBaseConfig interface [DirectShow],described, IVPBaseConfigInterface, dshow.ivpbaseconfig, vpconfig/IVPBaseConfig
req.header: vpconfig.h
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
 - IVPBaseConfig
 - vpconfig/IVPBaseConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig
---

# IVPBaseConfig interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<code>IVPBaseConfig</code> is implemented on a filter that wraps a hardware device such as a decoder or capture device, if the device has a video port to the graphics adapter. This interface allows the video port to communicate with the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter regarding configuration information. The <a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig</a> interface derives from this interface.

Applications should never use this interface.

## -inheritance

The <b>IVPBaseConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVPBaseConfig</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a>
