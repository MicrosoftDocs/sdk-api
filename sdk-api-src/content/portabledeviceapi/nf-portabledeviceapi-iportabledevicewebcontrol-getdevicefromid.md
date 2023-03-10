---
UID: NF:portabledeviceapi.IPortableDeviceWebControl.GetDeviceFromId
title: IPortableDeviceWebControl::GetDeviceFromId (portabledeviceapi.h)
description: Instantiates a WPD Automation Device object for a given WPD device identifier. (IPortableDeviceWebControl.GetDeviceFromId)
helpviewer_keywords: ["GetDeviceFromId","GetDeviceFromId method [WPD Automation]","GetDeviceFromId method [WPD Automation]","IPortableDeviceWebControl interface","IPortableDeviceWebControl interface [WPD Automation]","GetDeviceFromId method","IPortableDeviceWebControl.GetDeviceFromId","IPortableDeviceWebControl::GetDeviceFromId","portabledeviceapi/IPortableDeviceWebControl::GetDeviceFromId","wpdauto.iportabledevicewebcontrol_getdevicefromid"]
old-location: wpdauto\iportabledevicewebcontrol_getdevicefromid.htm
tech.root: wpdauto
ms.assetid: ba375082-3f4f-44d7-96d3-bf8151408b9e
ms.date: 12/05/2018
ms.keywords: GetDeviceFromId, GetDeviceFromId method [WPD Automation], GetDeviceFromId method [WPD Automation],IPortableDeviceWebControl interface, IPortableDeviceWebControl interface [WPD Automation],GetDeviceFromId method, IPortableDeviceWebControl.GetDeviceFromId, IPortableDeviceWebControl::GetDeviceFromId, portabledeviceapi/IPortableDeviceWebControl::GetDeviceFromId, wpdauto.iportabledevicewebcontrol_getdevicefromid
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [UWP apps only]
req.target-min-winversvr: Windows Server 2012 [UWP apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceWebControl::GetDeviceFromId
 - portabledeviceapi/IPortableDeviceWebControl::GetDeviceFromId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - portabledeviceapi.h
api_name:
 - IPortableDeviceWebControl.GetDeviceFromId
---

# IPortableDeviceWebControl::GetDeviceFromId


## -description

Instantiates a WPD Automation <a href="/previous-versions/windows/desktop/wiaaut/-wiaaut-device">Device</a> object for a given WPD device identifier.

## -parameters

### -param deviceId [in]

A <b>BSTR</b> that is used by Plug-and-play to identify a currently connected WPD device. The Plug and Play (PnP) identifier for a particular device can be obtained from the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">IPortableDeviceManager::GetDevices</a> method in the WPD C++/COM API.

A Windows Store app can obtain the PnP identifier of a WPD device by using <a href="/uwp/api/windows.devices.portable.servicedevice.getdeviceselector">Windows.Devices.Portable.ServiceDevice.GetDeviceSelector</a> or <a href="/uwp/api/windows.devices.portable.servicedevice.getdeviceselectorfromserviceid">Windows.Devices.Portable.ServiceDevice.GetDeviceSelectorFromServiceId</a> to get a selector string to pass to <a href="/uwp/api/windows.devices.enumeration.deviceinformation.findallasync">Windows.Devices.Enumeration.DeviceInformation.FindAllAsync</a>. <a href="/uwp/api/windows.devices.enumeration.deviceinformation.findallasync">FindAllAsync</a> returns a collection of <a href="/uwp/api/windows.devices.enumeration.deviceinformation">DeviceInformation</a> objects that represent the currently connected  WPD devices. A <b>DeviceInformation</b> object's <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-id-vb">Id</a> property is the device's PnP identifier.

### -param ppDevice [out, retval]

Contains a pointer to the <b>IDispatch</b> implementation for the WPD Automation <a href="/previous-versions/windows/desktop/wiaaut/-wiaaut-device">Device</a> object.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
A call to this method outside of a Windows Store app running on Windows 8 will return this error code.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  This method can only be used in Windows Store apps.</div>
<div> </div>

#### Examples

For WPD devices that use an MTP device service, you can create a COM Automation object to work with the device like this:


```javascript
deviceFactory = new ActiveXObject("PortableDeviceAutomation.Factory");
 
var device = deviceFactory.getDeviceFromId(deviceId);
// Get the first service on the device
var deviceService = device.services[0];
```

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicewebcontrol">IPortableDeviceWebControl</a>

<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PortableDeviceServices">Portable Device Service Sample</a>
