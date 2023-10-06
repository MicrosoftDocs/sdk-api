---
UID: NN:strmif.IAMDroppedFrames
title: IAMDroppedFrames (strmif.h)
description: The IAMDroppedFrames interface retrieves performance information from a video capture filter, including how many frames were dropped and how many were delivered. Applications can use this interface to determine capture performance at run-time.
helpviewer_keywords: ["IAMDroppedFrames","IAMDroppedFrames interface [DirectShow]","IAMDroppedFrames interface [DirectShow]","described","IAMDroppedFramesInterface","dshow.iamdroppedframes","strmif/IAMDroppedFrames"]
old-location: dshow\iamdroppedframes.htm
tech.root: dshow
ms.assetid: b41c3792-76fe-48e0-b2f5-ca3b0ee4c8ae
ms.date: 4/26/2023
ms.keywords: IAMDroppedFrames, IAMDroppedFrames interface [DirectShow], IAMDroppedFrames interface [DirectShow],described, IAMDroppedFramesInterface, dshow.iamdroppedframes, strmif/IAMDroppedFrames
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMDroppedFrames
 - strmif/IAMDroppedFrames
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
 - IAMDroppedFrames
---

# IAMDroppedFrames interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IAMDroppedFrames</b> interface retrieves performance information from a video capture filter, including how many frames were dropped and how many were delivered. Applications can use this interface to determine capture performance at run-time.

## -inheritance

The <b>IAMDroppedFrames</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDroppedFrames</b> also has these types of members:

## -remarks

Some filters that expose this interface do not implement the <a href="/windows/desktop/api/strmif/nf-strmif-iamdroppedframes-getdroppedinfo">GetDroppedInfo</a> or <a href="/windows/desktop/api/strmif/nf-strmif-iamdroppedframes-getaverageframesize">GetAverageFrameSize</a> method.

For Windows Driver Model (WDM) devices, the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="/windows-hardware/drivers/stream/propsetid-vidcap-droppedframes">PROPSETID_VIDCAP_DROPPEDFRAMES</a> property set. For more information, see the <a href="/windows-hardware/drivers/gettingstarted/">Windows Driver Kit (WDK)</a> documentation.

The number of dropped frames is reported by the capture driver. This information is not directly correlated with any particular media sample, so it is not accurate on a per-frame basis, although it should be accurate over time.

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
