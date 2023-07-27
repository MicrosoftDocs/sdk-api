---
UID: NN:strmif.IVMRDeinterlaceControl
title: IVMRDeinterlaceControl (strmif.h)
description: The IVMRDeinterlaceControl interface provides support for advanced hardware-accelerated deinterlacing using the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRDeinterlaceControl","IVMRDeinterlaceControl interface [DirectShow]","IVMRDeinterlaceControl interface [DirectShow]","described","IVMRDeinterlaceControlInterface","dshow.ivmrdeinterlacecontrol","strmif/IVMRDeinterlaceControl"]
old-location: dshow\ivmrdeinterlacecontrol.htm
tech.root: dshow
ms.assetid: 77abbcd4-6538-491d-b3c2-6a29a391c68a
ms.date: 4/26/2023
ms.keywords: IVMRDeinterlaceControl, IVMRDeinterlaceControl interface [DirectShow], IVMRDeinterlaceControl interface [DirectShow],described, IVMRDeinterlaceControlInterface, dshow.ivmrdeinterlacecontrol, strmif/IVMRDeinterlaceControl
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
 - IVMRDeinterlaceControl
 - strmif/IVMRDeinterlaceControl
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
 - IVMRDeinterlaceControl
---

# IVMRDeinterlaceControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IVMRDeinterlaceControl</b> interface provides support for advanced hardware-accelerated deinterlacing using the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). This interface enables applications or other filters to control how the VMR manages DirectX Video Acceleration (DirectX VA) hardware deinterlacing.

## -inheritance

The <b>IVMRDeinterlaceControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRDeinterlaceControl</b> also has these types of members:

## -remarks

This interface is applicable only when the VMR is in mixer mode. All methods in this interface return VFW_E_VMR_NOT_IN_MIXER_MODE if the VMR is not in mixer mode.

Deinterlacing modes are identified by GUIDs. The graphics device driver returns an array of GUIDs for the modes that it supports. The array is sorted in order of quality, from best quality to lowest quality. To retrieve the list of GUIDs, call the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getnumberofdeinterlacemodes">GetNumberOfDeinterlaceModes</a> method. To obtain more information about a particular mode, pass this GUID to the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlacemodecaps">GetDeinterlaceModeCaps</a> method. To configure the VMR to use a particular mode, call the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-setdeinterlacemode">SetDeinterlaceMode</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/setting-deinterlace-preferences">Setting Deinterlace Preferences</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
