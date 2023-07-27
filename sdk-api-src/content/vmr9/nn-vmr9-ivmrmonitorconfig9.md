---
UID: NN:vmr9.IVMRMonitorConfig9
title: IVMRMonitorConfig9 (vmr9.h)
description: The IVMRMonitorConfig9 interface is implemented by the Video Mixing Renderer Filter 9 (VMR-9).
helpviewer_keywords: ["IVMRMonitorConfig9","IVMRMonitorConfig9 interface [DirectShow]","IVMRMonitorConfig9 interface [DirectShow]","described","IVMRMonitorConfig9Interface","dshow.ivmrmonitorconfig9","vmr9/IVMRMonitorConfig9"]
old-location: dshow\ivmrmonitorconfig9.htm
tech.root: dshow
ms.assetid: 27a3a598-d8de-48b2-8b8c-6b5497db4c6c
ms.date: 4/26/2023
ms.keywords: IVMRMonitorConfig9, IVMRMonitorConfig9 interface [DirectShow], IVMRMonitorConfig9 interface [DirectShow],described, IVMRMonitorConfig9Interface, dshow.ivmrmonitorconfig9, vmr9/IVMRMonitorConfig9
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
 - IVMRMonitorConfig9
 - vmr9/IVMRMonitorConfig9
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
 - IVMRMonitorConfig9
---

# IVMRMonitorConfig9 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRMonitorConfig9</code> interface is implemented by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). Applications use this interface to determine the capabilities of the display devices on the system and to control which device is used to display the output. For example, if the system contains a hardware DVD decoder and the VMR is rendering the output from that decoder, then on a multi-monitor system, an application must use this interface to specify the display device that is connected to the decoder.

The VMR-9 supports a maximum of 16 display devices.

## -inheritance

The <b>IVMRMonitorConfig9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRMonitorConfig9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
