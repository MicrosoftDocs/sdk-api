---
UID: NF:amvideo.IFullScreenVideoEx.GetAcceleratorTable
title: IFullScreenVideoEx::GetAcceleratorTable (amvideo.h)
description: The GetAcceleratorTable method retrieves the accelerator table currently being used to translate keyboard messages. The Full Screen Renderer filter does not support this method.
helpviewer_keywords: ["GetAcceleratorTable","GetAcceleratorTable method [DirectShow]","GetAcceleratorTable method [DirectShow]","IFullScreenVideoEx interface","IFullScreenVideoEx interface [DirectShow]","GetAcceleratorTable method","IFullScreenVideoEx.GetAcceleratorTable","IFullScreenVideoEx::GetAcceleratorTable","IFullScreenVideoExGetAcceleratorTable","amvideo/IFullScreenVideoEx::GetAcceleratorTable","dshow.ifullscreenvideoex_getacceleratortable"]
old-location: dshow\ifullscreenvideoex_getacceleratortable.htm
tech.root: dshow
ms.assetid: 60d1246b-8719-4f41-9088-2672f51dd6a9
ms.date: 4/26/2023
ms.keywords: GetAcceleratorTable, GetAcceleratorTable method [DirectShow], GetAcceleratorTable method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetAcceleratorTable method, IFullScreenVideoEx.GetAcceleratorTable, IFullScreenVideoEx::GetAcceleratorTable, IFullScreenVideoExGetAcceleratorTable, amvideo/IFullScreenVideoEx::GetAcceleratorTable, dshow.ifullscreenvideoex_getacceleratortable
req.header: amvideo.h
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
 - IFullScreenVideoEx::GetAcceleratorTable
 - amvideo/IFullScreenVideoEx::GetAcceleratorTable
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
 - IFullScreenVideoEx.GetAcceleratorTable
---

# IFullScreenVideoEx::GetAcceleratorTable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAcceleratorTable</code> method retrieves the accelerator table currently being used to translate keyboard messages. The Full Screen Renderer filter does not support this method.

## -parameters

### -param phwnd [out]

Pointer to a variable that receives a window handle. The window receives translated messages.

### -param phAccel [out]

Pointer to a variable that receives a handle to the accelerator table.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>