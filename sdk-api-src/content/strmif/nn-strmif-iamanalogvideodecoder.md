---
UID: NN:strmif.IAMAnalogVideoDecoder
title: IAMAnalogVideoDecoder (strmif.h)
description: The IAMAnalogVideoDecoder interface sets and retrieves information about the analog-to-digital conversion process in a video capture filter.The WDM Video Capture filter exposes this interface if the device is an analog video capture device.
helpviewer_keywords: ["IAMAnalogVideoDecoder","IAMAnalogVideoDecoder interface [DirectShow]","IAMAnalogVideoDecoder interface [DirectShow]","described","IAMAnalogVideoDecoderInterface","dshow.iamanalogvideodecoder","strmif/IAMAnalogVideoDecoder"]
old-location: dshow\iamanalogvideodecoder.htm
tech.root: dshow
ms.assetid: 81d43941-7c81-4220-915f-0b373a7455e5
ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoDecoder, IAMAnalogVideoDecoder interface [DirectShow], IAMAnalogVideoDecoder interface [DirectShow],described, IAMAnalogVideoDecoderInterface, dshow.iamanalogvideodecoder, strmif/IAMAnalogVideoDecoder
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
 - IAMAnalogVideoDecoder
 - strmif/IAMAnalogVideoDecoder
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
 - IAMAnalogVideoDecoder
---

# IAMAnalogVideoDecoder interface


## -description

The <b>IAMAnalogVideoDecoder</b> interface sets and retrieves information about the analog-to-digital conversion process in a video capture filter.

The <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture</a> filter exposes this interface if the device is an analog video capture device. Applications can use this interface to control aspects of the analog decoding process, such as the analog video format and the horizontal sync lock.

## -inheritance

The <b>IAMAnalogVideoDecoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAnalogVideoDecoder</b> also has these types of members:

## -remarks

For Windows Driver Model (WDM) devices, the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="/windows-hardware/drivers/stream/propsetid-vidcap-videodecoder">PROPSETID_VIDCAP_VIDEODECODER</a> property set. For more information, see the <a href="/windows-hardware/drivers/gettingstarted/">Windows Driver Kit (WDK)</a> documentation.

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
