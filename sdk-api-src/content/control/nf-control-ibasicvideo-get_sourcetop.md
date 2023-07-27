---
UID: NF:control.IBasicVideo.get_SourceTop
title: IBasicVideo::get_SourceTop (control.h)
description: The get_SourceTop method retrieves the y-coordinate of the source rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","get_SourceTop method","IBasicVideo.get_SourceTop","IBasicVideo::get_SourceTop","IBasicVideoget_SourceTop","control/IBasicVideo::get_SourceTop","dshow.ibasicvideo_get_sourcetop","get_SourceTop","get_SourceTop method [DirectShow]","get_SourceTop method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_get_sourcetop.htm
tech.root: dshow
ms.assetid: 87ad3699-5a1b-4fa0-b7bd-5ec87758e9fa
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],get_SourceTop method, IBasicVideo.get_SourceTop, IBasicVideo::get_SourceTop, IBasicVideoget_SourceTop, control/IBasicVideo::get_SourceTop, dshow.ibasicvideo_get_sourcetop, get_SourceTop, get_SourceTop method [DirectShow], get_SourceTop method [DirectShow],IBasicVideo interface
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
 - IBasicVideo::get_SourceTop
 - control/IBasicVideo::get_SourceTop
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
 - IBasicVideo.get_SourceTop
---

# IBasicVideo::get_SourceTop


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_SourceTop</code> method retrieves the y-coordinate of the source rectangle.

## -parameters

### -param pSourceTop [out]

Pointer a variable that receives the y-coordinate, in pixels.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>