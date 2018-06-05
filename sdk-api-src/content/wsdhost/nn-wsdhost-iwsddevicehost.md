---
UID: NN:wsdhost.IWSDDeviceHost
title: IWSDDeviceHost
author: windows-sdk-content
description: Represents a DPWS-compliant device.
old-location: ncd\iwsddevicehost.htm
old-project: WsdApi
ms.assetid: 497d0331-c88d-4381-8990-94227a9b9659
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSDDeviceHost, IWSDDeviceHost interface, IWSDDeviceHost interface,described, ncd.iwsddevicehost, wsdhost/IWSDDeviceHost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDDeviceHost
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceHost interface


## -description


Represents a DPWS-compliant device . The device host will announce its presence on the network using the WS-Discovery protocol. The device host will also automatically respond to discovery queries and metadata requests.

The caller can register user-implemented services with the device host. These services will be exposed in the device metadata and the services will be available over the network. Messages bound for these services will be automatically dispatched into the service object.

Call <a href="https://msdn.microsoft.com/dbe7ccd0-494d-4f6c-90f6-e729839d7008">WSDCreateDeviceHost</a> or <a href="https://msdn.microsoft.com/8136fc01-9476-4ee4-aa44-784bef482ff5">WSDCreateDeviceHostAdvanced</a> to create an object that exposes this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDDeviceHost</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDDeviceHost</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0ef7760d-39eb-48fe-a7e9-043c2b9ba5a4">AddDynamicService</a>
</td>
<td align="left" width="63%">
Registers a service object for incoming requests, but does not add the service to the device host metadata. This is used for transient (dynamic) services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Initializes an instance of an <b>IWSDDeviceHost</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d514babb-c502-4d9a-b6c8-f371465cb9e8">RegisterPortType</a>
</td>
<td align="left" width="63%">
Registers a port type for incoming messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e125e72-4060-4be6-b370-b2f6b24d9da7">RegisterService</a>
</td>
<td align="left" width="63%">
Registers a service object for incoming requests and adds the service to the device host metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45c314d3-966b-4b90-ab23-fec2a8e4bc0f">RemoveDynamicService</a>
</td>
<td align="left" width="63%">
Unregisters a service object that was registered using <a href="https://msdn.microsoft.com/0ef7760d-39eb-48fe-a7e9-043c2b9ba5a4">AddDynamicService</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7832c787-f268-44e3-b394-363299b6a823">RetireService</a>
</td>
<td align="left" width="63%">
Unregisters a service object that was registered using  <a href="https://msdn.microsoft.com/8e125e72-4060-4be6-b370-b2f6b24d9da7">RegisterService</a> and removes the service from the device host metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc4cbed9-9ec4-4bbd-b1c9-89c4c11ff424">SetMetadata</a>
</td>
<td align="left" width="63%">
Sets the metadata for a device, excluding user-defined service metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f6aa8f6-3b7a-4d13-a052-c73f21823661">SetServiceDiscoverable</a>
</td>
<td align="left" width="63%">
Controls whether or not the service is advertised
    using WS-Discovery.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4cba7f0-6f08-43d7-b255-d3dfb1b5287d">SignalEvent</a>
</td>
<td align="left" width="63%">
Notifies all subscribed clients that an event has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts the device host and publishes the device host using a WS-Discovery Hello message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Sends a WS-Discovery Bye message and stops the host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a8df6fb-2834-44f4-9f25-454dcc2ff660">Terminate</a>
</td>
<td align="left" width="63%">
Terminates the host and releases any attached services.

</td>
</tr>
</table> 


## -remarks




After retrieving this interface, the application would then:

<ol>
<li>Call the <a href="https://msdn.microsoft.com/d514babb-c502-4d9a-b6c8-f371465cb9e8">RegisterPortType</a> method to register all necessary port types.</li>
<li>Call <a href="https://msdn.microsoft.com/dc4cbed9-9ec4-4bbd-b1c9-89c4c11ff424">SetMetadata</a> to describe the device and optionally call <a href="https://msdn.microsoft.com/8e125e72-4060-4be6-b370-b2f6b24d9da7">RegisterService</a> one or more times to register services described in the service host metadata.</li>
<li>Call the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a> method to start the device host and to publish the device using WS-Discovery.After starting the device host, you can optionally:

<ol>
<li>Call <a href="https://msdn.microsoft.com/0ef7760d-39eb-48fe-a7e9-043c2b9ba5a4">AddDynamicService</a> for services not described in the service host metadata (for example, an ad hoc print job).</li>
<li>Call <a href="https://msdn.microsoft.com/7832c787-f268-44e3-b394-363299b6a823">RetireService</a> to terminate action on and disconnect a service activated by the <a href="https://msdn.microsoft.com/8e125e72-4060-4be6-b370-b2f6b24d9da7">RegisterService</a> method.</li>
<li>Call the <a href="https://msdn.microsoft.com/c4cba7f0-6f08-43d7-b255-d3dfb1b5287d">SignalEvent</a> method to indicate that notifications should be sent for subscriptions relating to a particular event.</li>
</ol>
</li>
<li>Call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a> method to terminate host execution and terminate publication of the device.</li>
</ol>


An <b>IWSDDeviceHost</b> object can provide an object for a service on demand (using a notification callback) when calling the host receives a request message directed at that service.






## -see-also




<a href="https://msdn.microsoft.com/2b23d7d3-3b06-48c8-993e-49c72b139624">Overview of the WSDAPI Interfaces</a>
 

 

