---
UID: NN:strmif.IVMRWindowlessControl
title: IVMRWindowlessControl (strmif.h)
description: The IVMRWindowlessControl interface controls how the Video Mixing Renderer Filter 7 (VMR-7) renders a video stream within a container window.
helpviewer_keywords: ["IVMRWindowlessControl","IVMRWindowlessControl interface [DirectShow]","IVMRWindowlessControl interface [DirectShow]","described","IVMRWindowlessControlInterface","dshow.ivmrwindowlesscontrol","strmif/IVMRWindowlessControl"]
old-location: dshow\ivmrwindowlesscontrol.htm
tech.root: dshow
ms.assetid: c21c5611-f376-4899-9914-c14a18af3810
ms.date: 4/26/2023
ms.keywords: IVMRWindowlessControl, IVMRWindowlessControl interface [DirectShow], IVMRWindowlessControl interface [DirectShow],described, IVMRWindowlessControlInterface, dshow.ivmrwindowlesscontrol, strmif/IVMRWindowlessControl
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
 - IVMRWindowlessControl
 - strmif/IVMRWindowlessControl
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
 - IVMRWindowlessControl
---

# IVMRWindowlessControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRWindowlessControl</code> interface controls how the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7) renders a video stream within a container window. Applications must first put the VMR-7 into windowless mode before using this interface.

For the VMR-9, use the IVMRWindowlessControl9 interface.

## -inheritance

The <b>IVMRWindowlessControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRWindowlessControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
