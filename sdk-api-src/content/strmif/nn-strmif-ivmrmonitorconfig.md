---
UID: NN:strmif.IVMRMonitorConfig
title: IVMRMonitorConfig (strmif.h)
description: The IVMRMonitorConfig interface is implemented by the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRMonitorConfig","IVMRMonitorConfig interface [DirectShow]","IVMRMonitorConfig interface [DirectShow]","described","IVMRMonitorConfigInterface","dshow.ivmrmonitorconfig","strmif/IVMRMonitorConfig"]
old-location: dshow\ivmrmonitorconfig.htm
tech.root: dshow
ms.assetid: 02b4016b-a65b-41ac-b5c6-e5f6825f179c
ms.date: 4/26/2023
ms.keywords: IVMRMonitorConfig, IVMRMonitorConfig interface [DirectShow], IVMRMonitorConfig interface [DirectShow],described, IVMRMonitorConfigInterface, dshow.ivmrmonitorconfig, strmif/IVMRMonitorConfig
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
 - IVMRMonitorConfig
 - strmif/IVMRMonitorConfig
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
 - IVMRMonitorConfig
---

# IVMRMonitorConfig interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRMonitorConfig</code> interface is implemented by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). Applications use this interface to determine the capabilities of the display devices on the system and to control which device is used to display the output. For example, if the system contains a hardware DVD decoder and the VMR is rendering the output from that decoder, then on a multi-monitor system, an application must use this interface to specify the display device that is connected to the decoder.

The VMR-7 supports a maximum of 15 display devices.

It is the responsibility of the application to ensure that the playback window is positioned on the desired monitor before the window is displayed. Otherwise the playback window will be displayed at a location chosen by the Windows Shell (Explorer) which may not be on the desired monitor.

For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmonitorconfig9">IVMRMonitorConfig9</a> interface.

## -inheritance

The <b>IVMRMonitorConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRMonitorConfig</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
