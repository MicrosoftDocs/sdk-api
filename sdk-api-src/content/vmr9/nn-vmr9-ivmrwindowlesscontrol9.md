---
UID: NN:vmr9.IVMRWindowlessControl9
title: IVMRWindowlessControl9 (vmr9.h)
description: The IVMRWindowlessControl9 interface controls how the Video Mixing Renderer Filter 9 (VMR-9) renders a video stream within a container window.
helpviewer_keywords: ["IVMRWindowlessControl9","IVMRWindowlessControl9 interface [DirectShow]","IVMRWindowlessControl9 interface [DirectShow]","described","IVMRWindowlessControl9Interface","dshow.ivmrwindowlesscontrol9","vmr9/IVMRWindowlessControl9"]
old-location: dshow\ivmrwindowlesscontrol9.htm
tech.root: dshow
ms.assetid: 9db99c31-65b5-4ff1-9c0d-22140a3687e8
ms.date: 4/26/2023
ms.keywords: IVMRWindowlessControl9, IVMRWindowlessControl9 interface [DirectShow], IVMRWindowlessControl9 interface [DirectShow],described, IVMRWindowlessControl9Interface, dshow.ivmrwindowlesscontrol9, vmr9/IVMRWindowlessControl9
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
 - IVMRWindowlessControl9
 - vmr9/IVMRWindowlessControl9
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
 - IVMRWindowlessControl9
---

# IVMRWindowlessControl9 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IVMRWindowlessControl9</b> interface controls how the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9) renders a video stream within a container window.

## -inheritance

The <b>IVMRWindowlessControl9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRWindowlessControl9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The VMR-9 supports this interface in windowless and renderless modes only. In windowed mode, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> returns <b>E_NOINTERFACE</b>. For more information, see <a href="/windows/desktop/DirectShow/vmr-modes-of-operation">VMR Modes of Operation</a>.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
