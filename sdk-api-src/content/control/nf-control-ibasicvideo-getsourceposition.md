---
UID: NF:control.IBasicVideo.GetSourcePosition
title: IBasicVideo::GetSourcePosition (control.h)
description: The GetSourcePosition method retrieves the position of the source rectangle.
helpviewer_keywords: ["GetSourcePosition","GetSourcePosition method [DirectShow]","GetSourcePosition method [DirectShow]","IBasicVideo interface","IBasicVideo interface [DirectShow]","GetSourcePosition method","IBasicVideo.GetSourcePosition","IBasicVideo::GetSourcePosition","IBasicVideoGetSourcePosition","control/IBasicVideo::GetSourcePosition","dshow.ibasicvideo_getsourceposition"]
old-location: dshow\ibasicvideo_getsourceposition.htm
tech.root: dshow
ms.assetid: 4624e38c-63ff-4860-a899-c70e44e0f8aa
ms.date: 4/26/2023
ms.keywords: GetSourcePosition, GetSourcePosition method [DirectShow], GetSourcePosition method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetSourcePosition method, IBasicVideo.GetSourcePosition, IBasicVideo::GetSourcePosition, IBasicVideoGetSourcePosition, control/IBasicVideo::GetSourcePosition, dshow.ibasicvideo_getsourceposition
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
 - IBasicVideo::GetSourcePosition
 - control/IBasicVideo::GetSourcePosition
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
 - IBasicVideo.GetSourcePosition
---

# IBasicVideo::GetSourcePosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetSourcePosition</code> method retrieves the position of the source rectangle.

## -parameters

### -param pLeft [out]

Pointer to a variable that receives the x-coordinate, in pixels.

### -param pTop [out]

Pointer to a variable that receives the y-coordinate, in pixels.

### -param pWidth [out]

Pointer to a variable that receives the width, in pixels.

### -param pHeight [out]

Pointer to a variable that receives the height, in pixels.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method has the same effect as individually calling the <a href="/windows/desktop/api/control/nf-control-ibasicvideo-get_sourceleft">IBasicVideo::get_SourceLeft</a>, <a href="/windows/desktop/api/control/nf-control-ibasicvideo-get_sourcetop">IBasicVideo::get_SourceTop</a>, <a href="/windows/desktop/api/control/nf-control-ibasicvideo-get_sourcewidth">IBasicVideo::get_SourceWidth</a>, and <a href="/windows/desktop/api/control/nf-control-ibasicvideo-get_sourceheight">IBasicVideo::get_SourceHeight</a> methods.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>