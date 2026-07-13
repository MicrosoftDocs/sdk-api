---
UID: NN:strmif.IVMRImagePresenter
title: IVMRImagePresenter (strmif.h)
description: The IVMRImagePresenter interface is implemented by the default Allocator-Presenter for the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRImagePresenter","IVMRImagePresenter interface [DirectShow]","IVMRImagePresenter interface [DirectShow]","described","IVMRImagePresenterInterface","dshow.ivmrimagepresenter","strmif/IVMRImagePresenter"]
old-location: dshow\ivmrimagepresenter.htm
tech.root: dshow
ms.assetid: cb9b1e29-45c3-4208-8343-c2924505a9f3
ms.date: 4/26/2023
ms.keywords: IVMRImagePresenter, IVMRImagePresenter interface [DirectShow], IVMRImagePresenter interface [DirectShow],described, IVMRImagePresenterInterface, dshow.ivmrimagepresenter, strmif/IVMRImagePresenter
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
 - IVMRImagePresenter
 - strmif/IVMRImagePresenter
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
 - IVMRImagePresenter
---

# IVMRImagePresenter interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRImagePresenter</code> interface is implemented by the default Allocator-Presenter for the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). It must also be implemented by any plug-in Allocator-Presenter that an application provides for the VMR-7. The VMR-7 uses the methods on this interface to inform the Allocator-Presenter that it should present the video frame contained in the supplied Direct Draw surface. Applications do not use this interface.

For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenter9">IVMRImagePresenter9</a> interface.

## -inheritance

The <b>IVMRImagePresenter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRImagePresenter</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
