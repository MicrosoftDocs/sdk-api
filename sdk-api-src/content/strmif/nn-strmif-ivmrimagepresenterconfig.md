---
UID: NN:strmif.IVMRImagePresenterConfig
title: IVMRImagePresenterConfig (strmif.h)
description: The IVMRImagePresenterConfig interface provides methods for setting the rendering preferences on the allocator-presenter used by the Video Mixing Renderer Filter 7 (VMR-7).Applications should not use this interface directly.
helpviewer_keywords: ["IVMRImagePresenterConfig","IVMRImagePresenterConfig interface [DirectShow]","IVMRImagePresenterConfig interface [DirectShow]","described","IVMRImagePresenterConfigInterface","dshow.ivmrimagepresenterconfig","strmif/IVMRImagePresenterConfig"]
old-location: dshow\ivmrimagepresenterconfig.htm
tech.root: dshow
ms.assetid: cbf0fac4-c976-4c1a-ab3a-75ae0d565544
ms.date: 4/26/2023
ms.keywords: IVMRImagePresenterConfig, IVMRImagePresenterConfig interface [DirectShow], IVMRImagePresenterConfig interface [DirectShow],described, IVMRImagePresenterConfigInterface, dshow.ivmrimagepresenterconfig, strmif/IVMRImagePresenterConfig
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
 - IVMRImagePresenterConfig
 - strmif/IVMRImagePresenterConfig
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
 - IVMRImagePresenterConfig
---

# IVMRImagePresenterConfig interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRImagePresenterConfig</code> interface provides methods for setting the rendering preferences on the allocator-presenter used by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7).

Applications should not use this interface directly. The VMR-7 filter's <b>IVMRFilterConfig</b> interface calls methods on this interface. The default allocator-presenter implements this interface. Custom allocator-presenters can also expose this interface.

For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenterconfig9">IVMRImagePresenterConfig9</a> interface.

## -inheritance

The <b>IVMRImagePresenterConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRImagePresenterConfig</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
