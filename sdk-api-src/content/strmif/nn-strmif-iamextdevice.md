---
UID: NN:strmif.IAMExtDevice
title: IAMExtDevice (strmif.h)
description: The IAMExtDevice interface controls an external device, such as a DV camera or video tape recoder (VTR).
helpviewer_keywords: ["IAMExtDevice","IAMExtDevice interface [DirectShow]","IAMExtDevice interface [DirectShow]","described","IAMExtDeviceInterface","dshow.iamextdevice","strmif/IAMExtDevice"]
old-location: dshow\iamextdevice.htm
tech.root: dshow
ms.assetid: 0423e888-39d1-45cb-9bcf-722240a31fbd
ms.date: 12/05/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMExtDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMExtDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMExtDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-calibrate">Calibrate</a>
</td>
<td align="left" width="63%">
Calibrates the device's transport mechanism.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-get_deviceport">get_DevicePort</a>
</td>
<td align="left" width="63%">
Retrieves the communication port to which the device is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-get_devicepower">get_DevicePower</a>
</td>
<td align="left" width="63%">
Retrieves the device's power mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-get_externaldeviceid">get_ExternalDeviceID</a>
</td>
<td align="left" width="63%">
Retrieves the model number of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-get_externaldeviceversion">get_ExternalDeviceVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number of the device's operating software.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-getcapability">GetCapability</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-put_deviceport">put_DevicePort</a>
</td>
<td align="left" width="63%">
Specifies the communication port to which the device is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-put_devicepower">put_DevicePower</a>
</td>
<td align="left" width="63%">
Sets the device's power mode.

</td>
</tr>
</table>

## -remarks

The DV device drivers require some additional constants that are defined in the header file Xprtdefs.h.

For Windows Driver Model (WDM) devices, the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="/windows-hardware/drivers/stream/propsetid-ext-device">PROPSETID_EXT_DEVICE</a> property set. For more information, see the <a href="/windows-hardware/drivers/gettingstarted/">Windows Driver Kit (WDK)</a> documtenation.

<h3><a id="Hardware_Requirements"></a><a id="hardware_requirements"></a><a id="HARDWARE_REQUIREMENTS"></a>Hardware Requirements</h3>
To control an external VCR, certain hardware requirements are recommended. VCRs with an RS-422 serial interface require a special serial port card or an external RS-232-to-RS-422 adapter. In addition, for best performance, your computer should have a serial port card built with a 16550 high-performance UART (Universal Asynchronous Receiver/Transmitter) to sustain higher baud rates, such as 38.4 baud.

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>