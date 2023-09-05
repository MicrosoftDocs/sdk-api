---
UID: NN:strmif.IFilterMapper
title: IFilterMapper (strmif.h)
description: Note  This interface has been deprecated. (IFilterMapper)
helpviewer_keywords: ["IFilterMapper","IFilterMapper interface [DirectShow]","IFilterMapper interface [DirectShow]","described","IFilterMapperInterface","dshow.ifiltermapper","strmif/IFilterMapper"]
old-location: dshow\ifiltermapper.htm
tech.root: dshow
ms.assetid: e2f32235-e331-4c3c-925a-7cfa531e9ab3
ms.date: 4/26/2023
ms.keywords: IFilterMapper, IFilterMapper interface [DirectShow], IFilterMapper interface [DirectShow],described, IFilterMapperInterface, dshow.ifiltermapper, strmif/IFilterMapper
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IFilterMapper
 - strmif/IFilterMapper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IFilterMapper
---

# IFilterMapper interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface.</div>
<div> </div>
This interface provides methods for registering and unregistering filters, and for looking up filters based on their characteristics.

## -inheritance

The <b>IFilterMapper</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilterMapper</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
