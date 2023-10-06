---
UID: NN:vmr9.IVMRDeinterlaceControl9
title: IVMRDeinterlaceControl9 (vmr9.h)
description: The IVMRDeinterlaceControl9 interface supports hardware-accelerated deinterlacing using the Video Mixing Renderer Filter 9 (VMR-9).
helpviewer_keywords: ["IVMRDeinterlaceControl9","IVMRDeinterlaceControl9 interface [DirectShow]","IVMRDeinterlaceControl9 interface [DirectShow]","described","IVMRDeinterlaceControl9Interface","dshow.ivmrdeinterlacecontrol9","vmr9/IVMRDeinterlaceControl9"]
old-location: dshow\ivmrdeinterlacecontrol9.htm
tech.root: dshow
ms.assetid: 685f3627-30bd-4c78-9eda-0b06203dd46e
ms.date: 4/26/2023
ms.keywords: IVMRDeinterlaceControl9, IVMRDeinterlaceControl9 interface [DirectShow], IVMRDeinterlaceControl9 interface [DirectShow],described, IVMRDeinterlaceControl9Interface, dshow.ivmrdeinterlacecontrol9, vmr9/IVMRDeinterlaceControl9
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVMRDeinterlaceControl9
 - vmr9/IVMRDeinterlaceControl9
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
 - IVMRDeinterlaceControl9
---

# IVMRDeinterlaceControl9 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IVMRDeinterlaceControl9</b> interface supports hardware-accelerated deinterlacing using the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). This interface enables applications or other filters to control how the VMR manages DirectX Video Acceleration (DirectX VA) hardware deinterlacing.

## -inheritance

The <b>IVMRDeinterlaceControl9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRDeinterlaceControl9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Deinterlacing modes are identified by GUIDs. The graphics device driver returns an array of GUIDs for the modes that it supports. The array is sorted in order of quality, from best quality to lowest quality. To retrieve the list of GUIDs, call the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes">GetNumberOfDeinterlaceModes</a> method. To obtain more information about a particular mode, pass this GUID to the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps">GetDeinterlaceModeCaps</a> method. To configure the VMR to use a particular mode, call the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode">SetDeinterlaceMode</a> method.

To determine what de-interlacing modes are available, perform these steps:

<ol>
<li>Create the VMR-9 and put it into mixing mode.
      </li>
<li>Query the VMR-9 for the <b>IVMRDeinterlaceControl9</b> interface</li>
<li>Fill in a <a href="/windows/win32/api/strmif/ns-strmif-vmrvideodesc">VMRVideoDesc</a> structure that describes the format of the interlaced video.</li>
<li>Call <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes">IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes</a> to get the number of available de-interlacing modes.</li>
<li>For each mode returned, call <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps">IVMRDeinterlaceControl::GetDeinterlaceModeCaps</a> to get information about the mode.</li>
</ol>

## -see-also

<a href="/windows/desktop/DirectShow/setting-deinterlace-preferences">Setting Deinterlace Preferences</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>
