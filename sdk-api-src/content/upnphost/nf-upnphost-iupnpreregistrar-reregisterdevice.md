---
UID: NF:upnphost.IUPnPReregistrar.ReregisterDevice
title: IUPnPReregistrar::ReregisterDevice
author: windows-sdk-content
description: The ReregisterDevice method re-registers a device with the device host. The device information is stored by the device host. Then, the device host returns a device identifier and publishes and announces the device on the network.
old-location: upnp\iupnpreregistrar_reregisterdevice.htm
old-project: upnp
ms.assetid: 9f8a0a49-49e4-47b9-93bf-ca32cc80e243
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IUPnPReregistrar interface [UPnP APIs],ReregisterDevice method, IUPnPReregistrar.ReregisterDevice, IUPnPReregistrar::ReregisterDevice, ReregisterDevice, ReregisterDevice method [UPnP APIs], ReregisterDevice method [UPnP APIs],IUPnPReregistrar interface, _upnp_iupnpreregistrar_reregisterdevice, upnp.iupnpreregistrar_reregisterdevice, upnphost/IUPnPReregistrar::ReregisterDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnphost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPReregistrar.ReregisterDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPReregistrar::ReregisterDevice


## -description


The 
<b>ReregisterDevice</b> method re-registers a device with the device host. The device information is stored by the device host. Then, the device host returns a device identifier and publishes and announces the device on the network.


## -parameters




### -param bstrDeviceIdentifier [in]

Specifies the device identifier of the device. Use the identifier returned by 
<a href="https://msdn.microsoft.com/1bb99a42-143b-495a-8b02-efa7ca1d4d29">IUPnPRegistrar::RegisterDevice</a>.


### -param bstrXMLDesc [in]

Specifies the XML device description template of the device to register.


### -param bstrProgIDDeviceControlClass [in]

Specifies the ProgID of a device control object that implements the 
<a href="https://msdn.microsoft.com/c5d68459-f4ba-4df1-a00c-be86e24ce29f">IUPnPDeviceControl</a> interface. This interface must be an in-process COM server (CLSCTX_INPROC_SERVER) and must be accessible to <a href="https://msdn.microsoft.com/5409e2fe-a349-4739-a481-f8a35fd3c9b4">LocalService</a>.


### -param bstrInitString [in]

Identifies the initialization string specific to the device. This string is later passed to 
<a href="https://msdn.microsoft.com/0c1ea343-f04b-414d-92cf-044cb117bc9c">IUPnPDeviceControl::Initialize</a>.


### -param bstrContainerId [in]

Specifies a string that identifies the process group in which the device belongs. All devices with the same container ID are contained in the same process.


### -param bstrResourcePath [in]

Specifies the location of the resource directory of the device. This resource directory contains the icon files and service descriptions that are specified in the device description template <i>bstrXMLDesc</i>. The resource directory may also contain the presentation files. However, this is optional.


### -param nLifeTime [in]

Specifies the lifetime of the device announcement, in seconds. After the timeout expires, the announcements are refreshed. If you specify zero, the default value of 1800 (30 minutes) is used. The minimum allowable value is 900 (15 minutes); if you specify anything less than 900, an error is returned.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h, or one of the following UPnP-specific error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_NOTREGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The device has not been registered. Use <a href="https://msdn.microsoft.com/4b494b7e-4fcc-4de0-bdcc-96c68a5e0688">RegisterRunningDevice</a> to register an unregistered device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The device is currently running. Use <a href="https://msdn.microsoft.com/e5e9257e-1143-416c-8862-a69b726f5e23">ReregisterRunningDevice</a> to reregister a device while it is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DUPLICATE_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
A duplicate element exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DUPLICATE_SERVICE_ID</b></dt>
</dl>
</td>
<td width="60%">
A duplicate service ID for a service within the same parent device exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
The device description is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_ICON</b></dt>
</dl>
</td>
<td width="60%">
An error is present in the icon element of the device description.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
An error is present in a service element in the device description.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_REQUIRED_ELEMENT_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A required element is missing.

</td>
</tr>
</table>
 




## -remarks



Use the identifier returned in <i>pbstrDeviceIdentifier</i> when invoking 
<a href="https://msdn.microsoft.com/76fca00c-8638-4e2f-8dd1-20b24cde0108">IUPnPRegistrar::UnregisterDevice</a>.


Common errors that can occur when invoking this function include:

<ul>
<li>The necessary COM object was not found.</li>
<li>There is no access to the COM object for <a href="https://msdn.microsoft.com/5409e2fe-a349-4739-a481-f8a35fd3c9b4">LocalService</a>.</li>
<li>Subordinate COM interfaces.</li>
<li>The XML description limits (see 
<a href="https://msdn.microsoft.com/b2a7d342-958c-439d-8b17-b4fdc5fbad12">Creating a Device Description</a>).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/c851e102-4f03-4a21-9e62-9b5c60a728f3">IUPnPRegistrar</a>



<a href="https://msdn.microsoft.com/e01f325b-8fbd-43f2-a835-41cd3232f62e">IUPnPReregistrar</a>
 

 

