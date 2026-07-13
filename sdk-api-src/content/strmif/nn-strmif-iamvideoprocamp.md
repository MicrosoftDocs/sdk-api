---
UID: NN:strmif.IAMVideoProcAmp
title: IAMVideoProcAmp (strmif.h)
description: The IAMVideoProcAmp interface adjusts the qualities of an incoming video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.The WDM Video Capture filter exposes this interface if the hardware supports image adjustment.
helpviewer_keywords: ["IAMVideoProcAmp","IAMVideoProcAmp interface [DirectShow]","IAMVideoProcAmp interface [DirectShow]","described","IAMVideoProcAmpInterface","dshow.iamvideoprocamp","strmif/IAMVideoProcAmp"]
old-location: dshow\iamvideoprocamp.htm
tech.root: dshow
ms.assetid: 28c45790-2e5a-4acb-8a53-93f19c51dc6a
ms.date: 4/26/2023
ms.keywords: IAMVideoProcAmp, IAMVideoProcAmp interface [DirectShow], IAMVideoProcAmp interface [DirectShow],described, IAMVideoProcAmpInterface, dshow.iamvideoprocamp, strmif/IAMVideoProcAmp
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
 - IAMVideoProcAmp
 - strmif/IAMVideoProcAmp
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
 - IAMVideoProcAmp
---

# IAMVideoProcAmp interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IAMVideoProcAmp</b> interface adjusts the qualities of an incoming video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.

The <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture</a> filter exposes this interface if the hardware supports image adjustment.

## -inheritance

The <b>IAMVideoProcAmp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoProcAmp</b> also has these types of members:

## -remarks

For Windows Driver Model (WDM) devices, the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="/windows-hardware/drivers/stream/propsetid-vidcap-videoprocamp">PROPSETID_VIDCAP_VIDEOPROCAMP</a> property set. For more information, see the <a href="/windows-hardware/drivers/gettingstarted/">Windows Driver Kit (WDK)</a> documentation.

## -see-also

<a href="/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
