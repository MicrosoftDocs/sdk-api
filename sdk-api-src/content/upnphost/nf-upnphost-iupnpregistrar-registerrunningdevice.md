---
UID: NF:upnphost.IUPnPRegistrar.RegisterRunningDevice
title: IUPnPRegistrar::RegisterRunningDevice (upnphost.h)
description: The RegisterRunningDevice method registers a running device with the device host.
helpviewer_keywords: ["IUPnPRegistrar interface [UPnP APIs]","RegisterRunningDevice method","IUPnPRegistrar.RegisterRunningDevice","IUPnPRegistrar::RegisterRunningDevice","RegisterRunningDevice","RegisterRunningDevice method [UPnP APIs]","RegisterRunningDevice method [UPnP APIs]","IUPnPRegistrar interface","_upnp_iupnpregistrar_registerrunningdevice","upnp.iupnpregistrar_registerrunningdevice","upnphost/IUPnPRegistrar::RegisterRunningDevice"]
old-location: upnp\iupnpregistrar_registerrunningdevice.htm
tech.root: upnp
ms.assetid: 4b494b7e-4fcc-4de0-bdcc-96c68a5e0688
ms.date: 12/05/2018
ms.keywords: IUPnPRegistrar interface [UPnP APIs],RegisterRunningDevice method, IUPnPRegistrar.RegisterRunningDevice, IUPnPRegistrar::RegisterRunningDevice, RegisterRunningDevice, RegisterRunningDevice method [UPnP APIs], RegisterRunningDevice method [UPnP APIs],IUPnPRegistrar interface, _upnp_iupnpregistrar_registerrunningdevice, upnp.iupnpregistrar_registerrunningdevice, upnphost/IUPnPRegistrar::RegisterRunningDevice
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
 - IUPnPRegistrar::RegisterRunningDevice
 - upnphost/IUPnPRegistrar::RegisterRunningDevice
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
 - IUPnPRegistrar.RegisterRunningDevice
---

# IUPnPRegistrar::RegisterRunningDevice


## -description

The 
<b>RegisterRunningDevice</b> method registers a running device with the device host. The device information is stored by the device host. Then, the device host returns a device identifier and publishes and announces the device on the network. The publication of this device does not persist across system boots.

## -parameters

### -param bstrXMLDesc [in]

Specifies the XML device description template of the device to register.

### -param punkDeviceControl [in]

Specifies the <b>IUnknown</b> pointer to the device's device control object.

### -param bstrInitString [in]

Identifies the initialization string specific to the device. This string is later passed to 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-initialize">IUPnPDeviceControl::Initialize</a>.

### -param bstrResourcePath [in]

Specifies the location of the resource directory of the device. This resource directory contains the icon files and service descriptions that are specified in the device description template <i>bstrXMLDesc</i>.

### -param nLifeTime [in]

Specifies the lifetime of the device announcement, in seconds. After the timeout expires, the announcements are refreshed. If you specify zero, the default value of 1800 (30 minutes) is used. The minimum allowable value is 900 (15 minutes); if you specify anything less than 900, an error is returned.

### -param pbstrDeviceIdentifier [out]

Receives the device identifier. Use this identifier when unregistering or re-registering the device. Save this Device ID; you must use it when calling 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-unregisterdevice">UnregisterDevice</a>.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h, or one of the following UPnP-specific error codes.

<div class="alert"><b>Note</b>  If bstrResourcePath is too long, this method returns the value 0x80070002.</div>
<div> </div>
<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

The client that invokes this method must be able to impersonate <a href="/windows/desktop/Services/localservice-account">LocalService</a> in order to complete the processing of this method.

The 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-initialize">IUPnPDeviceControl::Initialize</a> method is invoked when the first control or event request is received.

Use the identifier returned in <i>pbstrDeviceIdentifier</i> when invoking 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-unregisterdevice">UnregisterDevice</a> or 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice">IUPnPReregistrar::ReregisterRunningDevice</a>.

The registration of this device does not persist across system boots.


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