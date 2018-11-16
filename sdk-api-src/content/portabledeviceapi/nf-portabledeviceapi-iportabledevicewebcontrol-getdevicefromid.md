---
UID: NF:portabledeviceapi.IPortableDeviceWebControl.GetDeviceFromId
title: IPortableDeviceWebControl::GetDeviceFromId
author: windows-sdk-content
description: Instantiates a WPD Automation Device object for a given WPD device identifier.
old-location: wpdauto\iportabledevicewebcontrol_getdevicefromid.htm
tech.root: wpdauto
ms.assetid: ba375082-3f4f-44d7-96d3-bf8151408b9e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetDeviceFromId, GetDeviceFromId method [WPD Automation], GetDeviceFromId method [WPD Automation],IPortableDeviceWebControl interface, IPortableDeviceWebControl interface [WPD Automation],GetDeviceFromId method, IPortableDeviceWebControl.GetDeviceFromId, IPortableDeviceWebControl::GetDeviceFromId, portabledeviceapi/IPortableDeviceWebControl::GetDeviceFromId, wpdauto.iportabledevicewebcontrol_getdevicefromid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - portabledeviceapi.h
api_name:
 - IPortableDeviceWebControl.GetDeviceFromId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- portabledeviceapi.h
: 
- IPortableDeviceWebControl.GetDeviceFromId
: 
---

# IPortableDeviceWebControl::GetDeviceFromId


## -description


Instantiates a WPD Automation <a href="wpdauto.device_object_script">Device</a> object for a given WPD device identifier.


## -parameters




### -param deviceId [in]

A <b>BSTR</b> that is used by Plug-and-play to identify a currently connected WPD device. The Plug and Play (PnP) identifier for a particular device can be obtained from the <a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">IPortableDeviceManager::GetDevices</a> method in the WPD C++/COM API.

A Windows Store app can obtain the PnP identifier of a WPD device by using <a href="https://msdn.microsoft.com/83dddddf-ebf5-4922-9fa7-c438bffbd606">Windows.Devices.Portable.ServiceDevice.GetDeviceSelector</a> or <a href="https://msdn.microsoft.com/de88774f-5141-400a-b1c4-a397dc2882d8">Windows.Devices.Portable.ServiceDevice.GetDeviceSelectorFromServiceId</a> to get a selector string to pass to <a href="https://msdn.microsoft.com/540adf5c-8c36-404f-8c35-ba36af6dfe23">Windows.Devices.Enumeration.DeviceInformation.FindAllAsync</a>. <a href="https://msdn.microsoft.com/0d50757d-38fa-430d-9797-9b8ff3e0c082">FindAllAsync</a> returns a collection of <a href="https://msdn.microsoft.com/8a53fdec-5fbe-4958-806a-4f840e6de6b5">DeviceInformation</a> objects that represent the currently connected  WPD devices. A <b>DeviceInformation</b> object's <a href="https://msdn.microsoft.com/ca31a3bd-de02-41d8-9e91-4ac7d2d3faa2">Id</a> property is the device's PnP identifier.


### -param ppDevice [out, retval]

Contains a pointer to the <b>IDispatch</b> implementation for the WPD Automation <a href="wpdauto.device_object_script">Device</a> object.



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

<div class="code"><span codelanguage="JavaScript"><table>
<tr>
<th>JavaScript</th>
</tr>
<tr>
<td>
<pre>
 
deviceFactory = new ActiveXObject("PortableDeviceAutomation.Factory");
 
var device = deviceFactory.getDeviceFromId(deviceId);
// Get the first service on the device
var deviceService = device.services[0];
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0ec81d6a-3671-4c4e-b650-f251fa99f7ea">IPortableDeviceWebControl</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=266421">Portable Device Service Sample</a>
 

 

