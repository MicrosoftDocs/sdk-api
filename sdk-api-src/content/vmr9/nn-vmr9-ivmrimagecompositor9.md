---
UID: NN:vmr9.IVMRImageCompositor9
title: IVMRImageCompositor9 (vmr9.h)
description: The IVMRImageCompositor9 interface is implemented by the default compositor for the Video Mixing Renderer Filter 9 (VMR-9).
helpviewer_keywords: ["IVMRImageCompositor9","IVMRImageCompositor9 interface [DirectShow]","IVMRImageCompositor9 interface [DirectShow]","described","IVMRImageCompositor9Interface","dshow.ivmrimagecompositor9","vmr9/IVMRImageCompositor9"]
old-location: dshow\ivmrimagecompositor9.htm
tech.root: dshow
ms.assetid: 19fda7f2-000f-47d0-a7c7-d8421de418a2
ms.date: 4/26/2023
ms.keywords: IVMRImageCompositor9, IVMRImageCompositor9 interface [DirectShow], IVMRImageCompositor9 interface [DirectShow],described, IVMRImageCompositor9Interface, dshow.ivmrimagecompositor9, vmr9/IVMRImageCompositor9
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRImageCompositor9
 - vmr9/IVMRImageCompositor9
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
 - IVMRImageCompositor9
---

# IVMRImageCompositor9 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRImageCompositor9</code> interface is implemented by the default compositor for the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). It must also be implemented by any plug-in compositor that an application provides for the VMR-9. The VMR-9 calls the methods on this interface to inform the compositor that it should composite the incoming video frames into a single output frame. Applications do not use this interface.

## -inheritance

The <b>IVMRImageCompositor9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRImageCompositor9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
