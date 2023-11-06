---
UID: NN:strmif.IVMRMixerControl
title: IVMRMixerControl (strmif.h)
description: The IVMRMixerControl interface is enables an application to manipulate the incoming video streams on the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRMixerControl","IVMRMixerControl interface [DirectShow]","IVMRMixerControl interface [DirectShow]","described","IVMRMixerControlInterface","dshow.ivmrmixercontrol","strmif/IVMRMixerControl"]
old-location: dshow\ivmrmixercontrol.htm
tech.root: dshow
ms.assetid: 2aefaebc-14e7-4918-9256-c5e9e3449095
ms.date: 4/26/2023
ms.keywords: IVMRMixerControl, IVMRMixerControl interface [DirectShow], IVMRMixerControl interface [DirectShow],described, IVMRMixerControlInterface, dshow.ivmrmixercontrol, strmif/IVMRMixerControl
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
 - IVMRMixerControl
 - strmif/IVMRMixerControl
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
 - IVMRMixerControl
---

# IVMRMixerControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRMixerControl</code> interface is enables an application to manipulate the incoming video streams on the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). Although this interface is implemented on the filter, it is actually the mixer component that is being configured. For this reason, this interface is only available when the mixer has been loaded through a call to <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams">IVMRFilterConfig::SetNumberOfStreams</a>. This interface is intended for use by applications only; it should not be used by upstream filters.

For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9</a> interface.

## -inheritance

The <b>IVMRMixerControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRMixerControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
