---
UID: NN:strmif.IAMExtDevice
title: IAMExtDevice
author: windows-sdk-content
description: The IAMExtDevice interface controls an external device, such as a DV camera or video tape recoder (VTR).
old-location: dshow\iamextdevice.htm
old-project: DirectShow
ms.assetid: 0423e888-39d1-45cb-9bcf-722240a31fbd
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IAMExtDevice, IAMExtDevice interface [DirectShow], IAMExtDevice interface [DirectShow],described, IAMExtDeviceInterface, dshow.iamextdevice, strmif/IAMExtDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtDevice interface


## -description



The <b>IAMExtDevice</b> interface controls an external device, such as a DV camera or video tape recoder (VTR).



This interface controls basic device functions. Several other interfaces exist for controlling more specific functionality in a device:
<ul>
<li>
<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport</a>
</li>
<li>
<a href="https://msdn.microsoft.com/76c3f603-8abc-450a-adb2-f2a90cb1634d">IAMTimecodeReader</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7fe74fc2-03bd-43dd-917f-ee0149f1e17f">IAMTimecodeGenerator</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2edfc260-5bb6-475d-b8af-252e7c7a8552">IAMTimecodeDisplay</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMExtDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMExtDevice</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0c760669-c494-45bb-994e-5b4599db7de4">Calibrate</a>
</td>
<td align="left" width="63%">
Calibrates the device's transport mechanism.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/307ad6ee-1084-4a83-bb19-f766f2328a0d">get_DevicePort</a>
</td>
<td align="left" width="63%">
Retrieves the communication port to which the device is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f25aac8-13ad-4ea2-96df-351da4729666">get_DevicePower</a>
</td>
<td align="left" width="63%">
Retrieves the device's power mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2217b0b1-3663-438b-8951-d2d1d8404e9c">get_ExternalDeviceID</a>
</td>
<td align="left" width="63%">
Retrieves the model number of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66a98ad3-850a-4b41-a169-f971fde83266">get_ExternalDeviceVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number of the device's operating software.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4efed2b8-a62c-4a82-bc2d-c6d3a202263c">GetCapability</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb83ae40-875b-47c4-8e8e-944392ad0782">put_DevicePort</a>
</td>
<td align="left" width="63%">
Specifies the communication port to which the device is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cb0c200-aaf4-44fb-b217-6a44a36089b5">put_DevicePower</a>
</td>
<td align="left" width="63%">
Sets the device's power mode.

</td>
</tr>
</table> 


## -remarks



The DV device drivers require some additional constants that are defined in the header file Xprtdefs.h.

For Windows Driver Model (WDM) devices, the <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567795">PROPSETID_EXT_DEVICE</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documtenation.

<h3><a id="Hardware_Requirements"></a><a id="hardware_requirements"></a><a id="HARDWARE_REQUIREMENTS"></a>Hardware Requirements</h3>
To control an external VCR, certain hardware requirements are recommended. VCRs with an RS-422 serial interface require a special serial port card or an external RS-232-to-RS-422 adapter. In addition, for best performance, your computer should have a serial port card built with a 16550 high-performance UART (Universal Asynchronous Receiver/Transmitter) to sustain higher baud rates, such as 38.4 baud.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

