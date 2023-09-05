---
UID: NN:vmr9.IVMRAspectRatioControl9
title: IVMRAspectRatioControl9 (vmr9.h)
description: The IVMRAspectRatioControl9 interface controls whether the Video Mixing Renderer Filter 9 (VMR-9) preserves the aspect ratio of the source video.
helpviewer_keywords: ["IVMRAspectRatioControl9","IVMRAspectRatioControl9 interface [DirectShow]","IVMRAspectRatioControl9 interface [DirectShow]","described","IVMRAspectRatioControl9Interface","dshow.ivmraspectratiocontrol9","vmr9/IVMRAspectRatioControl9"]
old-location: dshow\ivmraspectratiocontrol9.htm
tech.root: dshow
ms.assetid: ae850eea-c283-4500-baa0-e26641576852
ms.date: 4/26/2023
ms.keywords: IVMRAspectRatioControl9, IVMRAspectRatioControl9 interface [DirectShow], IVMRAspectRatioControl9 interface [DirectShow],described, IVMRAspectRatioControl9Interface, dshow.ivmraspectratiocontrol9, vmr9/IVMRAspectRatioControl9
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
 - IVMRAspectRatioControl9
 - vmr9/IVMRAspectRatioControl9
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
 - IVMRAspectRatioControl9
---

# IVMRAspectRatioControl9 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRAspectRatioControl9</code> interface controls whether the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9) preserves the aspect ratio of the source video. This interface is available when the VMR is operating in either windowed or windowless modes. In windowless mode, the same functionality is provided by the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl</a> interface.

## -inheritance

The <b>IVMRAspectRatioControl9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRAspectRatioControl9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
