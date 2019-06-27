---
UID: NN:wsdhost.IWSDDeviceHost
title: IWSDDeviceHost (wsdhost.h)
author: windows-sdk-content
description: Represents a DPWS-compliant device.
old-location: ncd\iwsddevicehost.htm
tech.root: WsdApi
ms.assetid: 497d0331-c88d-4381-8990-94227a9b9659
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost, IWSDDeviceHost interface, IWSDDeviceHost interface,described, ncd.iwsddevicehost, wsdhost/IWSDDeviceHost
ms.topic: interface
f1_keywords: 
 - "wsdhost/IWSDDeviceHost"
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDDeviceHost interface


## -description


Represents a DPWS-compliant device . The device host will announce its presence on the network using the WS-Discovery protocol. The device host will also automatically respond to discovery queries and metadata requests.

The caller can register user-implemented services with the device host. These services will be exposed in the device metadata and the services will be available over the network. Messages bound for these services will be automatically dispatched into the service object.

Call <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-wsdcreatedevicehost">WSDCreateDeviceHost</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-wsdcreatedevicehostadvanced">WSDCreateDeviceHostAdvanced</a> to create an object that exposes this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDDeviceHost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDDeviceHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDDeviceHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-adddynamicservice">AddDynamicService</a>
</td>
<td align="left" width="63%">
Registers a service object for incoming requests, but does not add the service to the device host metadata. This is used for transient (dynamic) services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-init">Init</a>
</td>
<td align="left" width="63%">
Initializes an instance of an <b>IWSDDeviceHost</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerporttype">RegisterPortType</a>
</td>
<td align="left" width="63%">
Registers a port type for incoming messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">RegisterService</a>
</td>
<td align="left" width="63%">
Registers a service object for incoming requests and adds the service to the device host metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-removedynamicservice">RemoveDynamicService</a>
</td>
<td align="left" width="63%">
Unregisters a service object that was registered using <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-adddynamicservice">AddDynamicService</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-retireservice">RetireService</a>
</td>
<td align="left" width="63%">
Unregisters a service object that was registered using  <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">RegisterService</a> and removes the service from the device host metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-setmetadata">SetMetadata</a>
</td>
<td align="left" width="63%">
Sets the metadata for a device, excluding user-defined service metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-setservicediscoverable">SetServiceDiscoverable</a>
</td>
<td align="left" width="63%">
Controls whether or not the service is advertised
    using WS-Discovery.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-signalevent">SignalEvent</a>
</td>
<td align="left" width="63%">
Notifies all subscribed clients that an event has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-start">Start</a>
</td>
<td align="left" width="63%">
Starts the device host and publishes the device host using a WS-Discovery Hello message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-stop">Stop</a>
</td>
<td align="left" width="63%">
Sends a WS-Discovery Bye message and stops the host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-terminate">Terminate</a>
</td>
<td align="left" width="63%">
Terminates the host and releases any attached services.

</td>
</tr>
</table> 


## -remarks




After retrieving this interface, the application would then:

<ol>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerporttype">RegisterPortType</a> method to register all necessary port types.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-setmetadata">SetMetadata</a> to describe the device and optionally call <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">RegisterService</a> one or more times to register services described in the service host metadata.</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-start">Start</a> method to start the device host and to publish the device using WS-Discovery.After starting the device host, you can optionally:

<ol>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-adddynamicservice">AddDynamicService</a> for services not described in the service host metadata (for example, an ad hoc print job).</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-retireservice">RetireService</a> to terminate action on and disconnect a service activated by the <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">RegisterService</a> method.</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-signalevent">SignalEvent</a> method to indicate that notifications should be sent for subscriptions relating to a particular event.</li>
</ol>
</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-stop">Stop</a> method to terminate host execution and terminate publication of the device.</li>
</ol>


An <b>IWSDDeviceHost</b> object can provide an object for a service on demand (using a notification callback) when calling the host receives a request message directed at that service.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WsdApi/overview-of-the-wsdapi-interfaces">Overview of the WSDAPI Interfaces</a>
 

 

