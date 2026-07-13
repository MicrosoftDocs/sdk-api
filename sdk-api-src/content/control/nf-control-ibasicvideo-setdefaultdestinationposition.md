---
UID: NF:control.IBasicVideo.SetDefaultDestinationPosition
title: IBasicVideo::SetDefaultDestinationPosition (control.h)
description: The SetDefaultDestinationPosition method reverts to the default destination rectangle. After this method is called, the video renderer uses the entire window for playback.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","SetDefaultDestinationPosition method","IBasicVideo.SetDefaultDestinationPosition","IBasicVideo::SetDefaultDestinationPosition","IBasicVideoSetDefaultDestinationPosition","SetDefaultDestinationPosition","SetDefaultDestinationPosition method [DirectShow]","SetDefaultDestinationPosition method [DirectShow]","IBasicVideo interface","control/IBasicVideo::SetDefaultDestinationPosition","dshow.ibasicvideo_setdefaultdestinationposition"]
old-location: dshow\ibasicvideo_setdefaultdestinationposition.htm
tech.root: dshow
ms.assetid: 82ee1be5-4a58-4104-a8a5-3c3926e2f1d2
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],SetDefaultDestinationPosition method, IBasicVideo.SetDefaultDestinationPosition, IBasicVideo::SetDefaultDestinationPosition, IBasicVideoSetDefaultDestinationPosition, SetDefaultDestinationPosition, SetDefaultDestinationPosition method [DirectShow], SetDefaultDestinationPosition method [DirectShow],IBasicVideo interface, control/IBasicVideo::SetDefaultDestinationPosition, dshow.ibasicvideo_setdefaultdestinationposition
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
 - IBasicVideo::SetDefaultDestinationPosition
 - control/IBasicVideo::SetDefaultDestinationPosition
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
 - IBasicVideo.SetDefaultDestinationPosition
---

# IBasicVideo::SetDefaultDestinationPosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDefaultDestinationPosition</code> method reverts to the default destination rectangle. After this method is called, the video renderer uses the entire window for playback.



## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>
