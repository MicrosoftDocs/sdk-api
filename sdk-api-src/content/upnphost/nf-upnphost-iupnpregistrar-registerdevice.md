---
UID: NF:upnphost.IUPnPRegistrar.RegisterDevice
title: IUPnPRegistrar::RegisterDevice (upnphost.h)
description: The RegisterDevice method registers a device with the device host. The device information is stored by the device host. Then, the device host returns a device identifier and publishes and announces the device on the network.
helpviewer_keywords: ["IUPnPRegistrar interface [UPnP APIs]","RegisterDevice method","IUPnPRegistrar.RegisterDevice","IUPnPRegistrar::RegisterDevice","RegisterDevice","RegisterDevice method [UPnP APIs]","RegisterDevice method [UPnP APIs]","IUPnPRegistrar interface","_upnp_iupnpregistrar_registerdevice","upnp.iupnpregistrar_registerdevice","upnphost/IUPnPRegistrar::RegisterDevice"]
old-location: upnp\iupnpregistrar_registerdevice.htm
tech.root: upnp
ms.assetid: 1bb99a42-143b-495a-8b02-efa7ca1d4d29
ms.date: 12/05/2018
ms.keywords: IUPnPRegistrar interface [UPnP APIs],RegisterDevice method, IUPnPRegistrar.RegisterDevice, IUPnPRegistrar::RegisterDevice, RegisterDevice, RegisterDevice method [UPnP APIs], RegisterDevice method [UPnP APIs],IUPnPRegistrar interface, _upnp_iupnpregistrar_registerdevice, upnp.iupnpregistrar_registerdevice, upnphost/IUPnPRegistrar::RegisterDevice
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
req.lib: 
req.dll: Upnphost.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPRegistrar::RegisterDevice
 - upnphost/IUPnPRegistrar::RegisterDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPRegistrar.RegisterDevice
---

# IUPnPRegistrar::RegisterDevice


## -description

The 
<b>RegisterDevice</b> method registers a device with the device host. The device information is stored by the device host. Then, the device host returns a device identifier and publishes and announces the device on the network.

## -parameters

### -param bstrXMLDesc [in]

Specifies the XML device description template of the device to register.

### -param bstrProgIDDeviceControlClass [in]

Specifies the ProgID of a device control object that implements the 
<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpdevicecontrol">IUPnPDeviceControl</a> interface. This interface must be an in-process COM server (CLSCTX_INPROC_SERVER) and must be accessible to <a href="/windows/desktop/Services/localservice-account">LocalService</a>.

### -param bstrInitString [in]

Identifies the initialization string specific to the device. This string is later passed to 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-initialize">IUPnPDeviceControl::Initialize</a>.

### -param bstrContainerId [in]

Specifies a string that identifies the process group in which the device belongs. All devices with the same container ID are contained in the same process.

### -param bstrResourcePath [in]

Specifies the location of the resource directory of the device. This resource directory contains the icon files and service descriptions that are specified in the device description template <i>bstrXMLDesc</i>. The resource directory may also contain the presentation files. However, this is optional.

### -param nLifeTime [in]

Specifies the lifetime of the device announcement, in seconds. After the timeout expires, the announcements are refreshed. If you specify zero, the default value of 1800 (30 minutes) is used. The minimum allowable value is 900 (15 minutes); if you specify anything less than 900, an error is returned.

### -param pbstrDeviceIdentifier [out]

Receives the device identifier. Use this identifier when unregistering or re-registering the device. Save this Device ID; you must use it when calling 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-unregisterdevice">UnregisterDevice</a>.

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

A device is instantiated and 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-initialize">IUPnPDeviceControl::Initialize</a> is invoked when a control or event request is received.

Use the identifier returned in <i>pbstrDeviceIdentifier</i> when invoking 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-unregisterdevice">UnregisterDevice</a> or 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice">IUPnPReregistrar::ReregisterDevice</a>.


Common errors that can occur when invoking this function include:

<ul>
<li>The necessary COM object was not found.</li>
<li>There is no access to the COM object for <a href="/windows/desktop/Services/localservice-account">LocalService</a>.</li>
<li>Subordinate COM interfaces.</li>
<li>The XML description limits (see 
<a href="/windows/desktop/UPnP/creating-a-device-description">Creating a Device Description</a>).</li>
<li>Evented variables did not return success codes and the device was shut down.</li>
<li>The service description was invalid. Use validatesd.exe to ensure that service descriptions are valid.</li>
<li>The service did not implement IUPnPEventSource and did not return a success code to 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsource-advise">IUPnPEventSource::Advise</a> and the device was shut down.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpregistrar">IUPnPRegistrar</a>



<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-unregisterdevice">IUPnPRegistrar::UnregisterDevice</a>



<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpreregistrar">IUPnPReregistrar</a>