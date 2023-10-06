---
UID: NF:amvideo.IQualProp.get_FramesDrawn
title: IQualProp::get_FramesDrawn (amvideo.h)
description: The get_FramesDrawn method retrieves the number of frames actually drawn since streaming started.
helpviewer_keywords: ["IQualProp interface [DirectShow]","get_FramesDrawn method","IQualProp.get_FramesDrawn","IQualProp::get_FramesDrawn","IQualPropget_FramesDrawn","amvideo/IQualProp::get_FramesDrawn","dshow.iqualprop_get_framesdrawn","get_FramesDrawn","get_FramesDrawn method [DirectShow]","get_FramesDrawn method [DirectShow]","IQualProp interface"]
old-location: dshow\iqualprop_get_framesdrawn.htm
tech.root: dshow
ms.assetid: 5a5d4aee-dd35-432f-b6a6-4b1b59ad9b78
ms.date: 4/26/2023
ms.keywords: IQualProp interface [DirectShow],get_FramesDrawn method, IQualProp.get_FramesDrawn, IQualProp::get_FramesDrawn, IQualPropget_FramesDrawn, amvideo/IQualProp::get_FramesDrawn, dshow.iqualprop_get_framesdrawn, get_FramesDrawn, get_FramesDrawn method [DirectShow], get_FramesDrawn method [DirectShow],IQualProp interface
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
 - IQualProp::get_FramesDrawn
 - amvideo/IQualProp::get_FramesDrawn
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
 - IQualProp.get_FramesDrawn
---

# IQualProp::get_FramesDrawn


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_FramesDrawn</code> method retrieves the number of frames actually drawn since streaming started.

## -parameters

### -param pcFramesDrawn

Pointer to the number of frames drawn since streaming started.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-iqualprop">IQualProp Interface</a>