---
UID: NF:control.IBasicVideo.get_SourceHeight
title: IBasicVideo::get_SourceHeight (control.h)
description: The get_SourceHeight method retrieves the height of the source rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","get_SourceHeight method","IBasicVideo.get_SourceHeight","IBasicVideo::get_SourceHeight","IBasicVideoget_SourceHeight","control/IBasicVideo::get_SourceHeight","dshow.ibasicvideo_get_sourceheight","get_SourceHeight","get_SourceHeight method [DirectShow]","get_SourceHeight method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_get_sourceheight.htm
tech.root: dshow
ms.assetid: 3f4e779a-cfa9-496d-a021-d24ae3daa5b3
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],get_SourceHeight method, IBasicVideo.get_SourceHeight, IBasicVideo::get_SourceHeight, IBasicVideoget_SourceHeight, control/IBasicVideo::get_SourceHeight, dshow.ibasicvideo_get_sourceheight, get_SourceHeight, get_SourceHeight method [DirectShow], get_SourceHeight method [DirectShow],IBasicVideo interface
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
 - IBasicVideo::get_SourceHeight
 - control/IBasicVideo::get_SourceHeight
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
 - IBasicVideo.get_SourceHeight
---

# IBasicVideo::get_SourceHeight


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_SourceHeight</code> method retrieves the height of the source rectangle.

## -parameters

### -param pSourceHeight [out]

Pointer to a variable that receives the current height, in pixels.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>