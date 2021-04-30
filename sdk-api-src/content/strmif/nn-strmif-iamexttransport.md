---
UID: NN:strmif.IAMExtTransport
title: IAMExtTransport (strmif.h)
description: The IAMExtTransport interface controls the transport on a video tape recporder (VTR) or camcorder.
helpviewer_keywords: ["IAMExtTransport","IAMExtTransport interface [DirectShow]","IAMExtTransport interface [DirectShow]","described","IAMExtTransportInterface","dshow.iamexttransport","strmif/IAMExtTransport"]
old-location: dshow\iamexttransport.htm
tech.root: dshow
ms.assetid: 4ce48038-bfcf-4b1f-8053-3446929a5f06
ms.date: 12/05/2018
ms.keywords: IAMExtTransport, IAMExtTransport interface [DirectShow], IAMExtTransport interface [DirectShow],described, IAMExtTransportInterface, dshow.iamexttransport, strmif/IAMExtTransport
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
 - IAMExtTransport
 - strmif/IAMExtTransport
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
 - IAMExtTransport
---

# IAMExtTransport interface


## -description

The <b>IAMExtTransport</b> interface controls the transport on a video tape recporder (VTR) or camcorder. Applications can use this interface to play, record, or stop the transport; determine whether the transport contains media; and other transport-related functions. The implementation of this interface can vary, depending on the device. Some methods might return E_NOTIMPL if the device does not support them.

This interface also contains methods for non-linear editing through <i>edit events</i> and <i>edit property sets</i>. Currently, DirectShow does not provide any filters or drivers that implement this part of the interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMExtTransport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMExtTransport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

The DV device drivers require some additional constants that are defined in the header file Xprtdefs.h.

For Windows Driver Model (WDM) devices, the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="/windows-hardware/drivers/stream/propsetid-ext-transport">PROPSETID_EXT_TRANSPORT</a> property set. For more information, see the <a href="/windows-hardware/drivers/gettingstarted/">Windows Driver Kit (WDK)</a> documentation.

<h3><a id="Hardware_Requirements"></a><a id="hardware_requirements"></a><a id="HARDWARE_REQUIREMENTS"></a>Hardware Requirements</h3>
To control an external VCR, certain hardware requirements are recommended. VCRs with an RS-422 serial interface require a special serial port card or an external RS-232-to-RS-422 adapter. In addition, for best performance, your computer should have a serial port card built with a 16550 high-performance UART to sustain higher baud rates, such as 38.4 baud.

<h3><a id="Filter_Developers"></a><a id="filter_developers"></a><a id="FILTER_DEVELOPERS"></a>Filter Developers</h3>
Implement this interface if you are writing a filter that controls an external device with a transport, such as a VTR. If you implement this interface, you should implement the <a href="/windows/desktop/api/strmif/nn-strmif-iamextdevice">IAMExtDevice</a> interface as well.

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
