---
UID: NF:strmif.IVMRImageCompositor.SetStreamMediaType
title: IVMRImageCompositor::SetStreamMediaType (strmif.h)
description: The SetStreamMediaType method sets the media type for the input stream.
helpviewer_keywords: ["IVMRImageCompositor interface [DirectShow]","SetStreamMediaType method","IVMRImageCompositor.SetStreamMediaType","IVMRImageCompositor::SetStreamMediaType","IVMRImageCompositorSetStreamMediaType","SetStreamMediaType","SetStreamMediaType method [DirectShow]","SetStreamMediaType method [DirectShow]","IVMRImageCompositor interface","dshow.ivmrimagecompositor_setstreammediatype","strmif/IVMRImageCompositor::SetStreamMediaType"]
old-location: dshow\ivmrimagecompositor_setstreammediatype.htm
tech.root: dshow
ms.assetid: ea3ed291-d837-4d11-bc82-0a060b093b21
ms.date: 4/26/2023
ms.keywords: IVMRImageCompositor interface [DirectShow],SetStreamMediaType method, IVMRImageCompositor.SetStreamMediaType, IVMRImageCompositor::SetStreamMediaType, IVMRImageCompositorSetStreamMediaType, SetStreamMediaType, SetStreamMediaType method [DirectShow], SetStreamMediaType method [DirectShow],IVMRImageCompositor interface, dshow.ivmrimagecompositor_setstreammediatype, strmif/IVMRImageCompositor::SetStreamMediaType
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVMRImageCompositor::SetStreamMediaType
 - strmif/IVMRImageCompositor::SetStreamMediaType
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
 - IVMRImageCompositor.SetStreamMediaType
---

# IVMRImageCompositor::SetStreamMediaType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetStreamMediaType</code> method sets the media type for the input stream.

## -parameters

### -param dwStrmID

Specifies the input stream. The value must be from 1 through 16.

### -param pmt

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the media type.

### -param fTexture

If <b>TRUE</b>, specifies that the target surface is a Direct3D texture surface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>