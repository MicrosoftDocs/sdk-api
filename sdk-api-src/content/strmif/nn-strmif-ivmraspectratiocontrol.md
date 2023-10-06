---
UID: NN:strmif.IVMRAspectRatioControl
title: IVMRAspectRatioControl (strmif.h)
description: The IVMRAspectRatioControl interface controls whether the Video Mixing Renderer Filter 7 (VMR-7) preserves the aspect ratio of the source video.
helpviewer_keywords: ["IVMRAspectRatioControl","IVMRAspectRatioControl interface [DirectShow]","IVMRAspectRatioControl interface [DirectShow]","described","IVMRAspectRatioControlInterface","dshow.ivmraspectratiocontrol","strmif/IVMRAspectRatioControl"]
old-location: dshow\ivmraspectratiocontrol.htm
tech.root: dshow
ms.assetid: a341be9d-9801-4215-840d-7d581e9ec3cb
ms.date: 4/26/2023
ms.keywords: IVMRAspectRatioControl, IVMRAspectRatioControl interface [DirectShow], IVMRAspectRatioControl interface [DirectShow],described, IVMRAspectRatioControlInterface, dshow.ivmraspectratiocontrol, strmif/IVMRAspectRatioControl
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
 - IVMRAspectRatioControl
 - strmif/IVMRAspectRatioControl
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
 - IVMRAspectRatioControl
---

# IVMRAspectRatioControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRAspectRatioControl</code> interface controls whether the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7) preserves the aspect ratio of the source video. This interface is available when the VMR-7 is operating in either windowed or windowless modes. In windowless mode, the same functionality is provided by the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl</a> interface.

## -inheritance

The <b>IVMRAspectRatioControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRAspectRatioControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
