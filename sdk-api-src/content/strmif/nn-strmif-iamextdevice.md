---
UID: NN:strmif.IAMExtDevice
title: IAMExtDevice (strmif.h)
description: The IAMExtDevice interface controls an external device, such as a DV camera or video tape recoder (VTR).
helpviewer_keywords: ["IAMExtDevice","IAMExtDevice interface [DirectShow]","IAMExtDevice interface [DirectShow]","described","IAMExtDeviceInterface","dshow.iamextdevice","strmif/IAMExtDevice"]
old-location: dshow\iamextdevice.htm
tech.root: dshow
ms.assetid: 0423e888-39d1-45cb-9bcf-722240a31fbd
ms.date: 4/26/2023
ms.keywords: IAMExtDevice, IAMExtDevice interface [DirectShow], IAMExtDevice interface [DirectShow],described, IAMExtDeviceInterface, dshow.iamextdevice, strmif/IAMExtDevice
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
 - IAMExtDevice
 - strmif/IAMExtDevice
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
 - IAMExtDevice
---

# IAMExtDevice interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IAMExtDevice</b> interface controls an external device, such as a DV camera or video tape recoder (VTR).



This interface controls basic device functions. Several other interfaces exist for controlling more specific functionality in a device:
<ul>
<li>
<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport</a>
</li>
<li>
<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodereader">IAMTimecodeReader</a>
</li>
<li>
<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodegenerator">IAMTimecodeGenerator</a>
</li>
<li>
<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodedisplay">IAMTimecodeDisplay</a>
</li>
</ul>

## -inheritance

The <b>IAMExtDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMExtDevice</b> also has these types of members:

## -remarks

The DV device drivers require some additional constants that are defined in the header file Xprtdefs.h.

For Windows Driver Model (WDM) devices, the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="/windows-hardware/drivers/stream/propsetid-ext-device">PROPSETID_EXT_DEVICE</a> property set. For more information, see the <a href="/windows-hardware/drivers/gettingstarted/">Windows Driver Kit (WDK)</a> documentation.

<h3><a id="Hardware_Requirements"></a><a id="hardware_requirements"></a><a id="HARDWARE_REQUIREMENTS"></a>Hardware Requirements</h3>
To control an external VCR, certain hardware requirements are recommended. VCRs with an RS-422 serial interface require a special serial port card or an external RS-232-to-RS-422 adapter. In addition, for best performance, your computer should have a serial port card built with a 16550 high-performance UART (Universal Asynchronous Receiver/Transmitter) to sustain higher baud rates, such as 38.4 baud.

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
