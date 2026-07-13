---
UID: NN:amvideo.IQualProp
title: IQualProp (amvideo.h)
description: The IQualProp interface provides methods for retrieving performance information from video renderers.
helpviewer_keywords: ["IQualProp","IQualProp interface [DirectShow]","IQualProp interface [DirectShow]","described","IQualPropInterface","amvideo/IQualProp","dshow.iqualprop"]
old-location: dshow\iqualprop.htm
tech.root: dshow
ms.assetid: 428dfb97-0dfa-442c-819e-291e6a58f712
ms.date: 4/26/2023
ms.keywords: IQualProp, IQualProp interface [DirectShow], IQualProp interface [DirectShow],described, IQualPropInterface, amvideo/IQualProp, dshow.iqualprop
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
 - IQualProp
 - amvideo/IQualProp
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
 - IQualProp
---

# IQualProp interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IQualProp</b> interface provides methods for retrieving performance information from video renderers. The values returned through the interface are reset each time the filter is stopped. The <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter and the <a href="/windows/desktop/DirectShow/full-screen-renderer-filter">Full Screen Renderer</a> filter expose this interface.

Applications can use this interface to retrieve video performance information.

## -inheritance

The <b>IQualProp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQualProp</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
