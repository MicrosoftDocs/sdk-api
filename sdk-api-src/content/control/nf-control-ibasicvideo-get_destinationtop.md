---
UID: NF:control.IBasicVideo.get_DestinationTop
title: IBasicVideo::get_DestinationTop (control.h)
description: The get_DestinationTop method retrieves the y-coordinate of the destination rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","get_DestinationTop method","IBasicVideo.get_DestinationTop","IBasicVideo::get_DestinationTop","IBasicVideoget_DestinationTop","control/IBasicVideo::get_DestinationTop","dshow.ibasicvideo_get_destinationtop","get_DestinationTop","get_DestinationTop method [DirectShow]","get_DestinationTop method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_get_destinationtop.htm
tech.root: dshow
ms.assetid: 79690655-ac84-4119-9d87-799990424f00
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],get_DestinationTop method, IBasicVideo.get_DestinationTop, IBasicVideo::get_DestinationTop, IBasicVideoget_DestinationTop, control/IBasicVideo::get_DestinationTop, dshow.ibasicvideo_get_destinationtop, get_DestinationTop, get_DestinationTop method [DirectShow], get_DestinationTop method [DirectShow],IBasicVideo interface
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
 - IBasicVideo::get_DestinationTop
 - control/IBasicVideo::get_DestinationTop
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
 - IBasicVideo.get_DestinationTop
---

# IBasicVideo::get_DestinationTop


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_DestinationTop</code> method retrieves the y-coordinate of the destination rectangle.

## -parameters

### -param pDestinationTop [out]

Pointer to a variable that receives the y-coordinate, in pixels.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>