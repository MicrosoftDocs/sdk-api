---
UID: NN:control.IBasicVideo2
title: IBasicVideo2 (control.h)
description: The IBasicVideo2 interface extends the IBasicVideo interface.
helpviewer_keywords: ["IBasicVideo2","IBasicVideo2 interface [DirectShow]","IBasicVideo2 interface [DirectShow]","described","IBasicVideo2Interface","control/IBasicVideo2","dshow.ibasicvideo2"]
old-location: dshow\ibasicvideo2.htm
tech.root: dshow
ms.assetid: a21fe7b9-75db-4c5b-bb29-42d305f048a1
ms.date: 4/26/2023
ms.keywords: IBasicVideo2, IBasicVideo2 interface [DirectShow], IBasicVideo2 interface [DirectShow],described, IBasicVideo2Interface, control/IBasicVideo2, dshow.ibasicvideo2
req.header: control.h
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
 - IBasicVideo2
 - control/IBasicVideo2
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
 - IBasicVideo2
---

# IBasicVideo2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IBasicVideo2</code> interface extends the <a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo</a> interface. The <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter and Video Mixing Renderer filters implement this interface, but the interface is exposed to applications through the Filter Graph Manager. Applications should always retrieve this interface from the Filter Graph Manager.

## -inheritance

The <b>IBasicVideo2</b> interface inherits from <a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo</a>. <b>IBasicVideo2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo</a>
