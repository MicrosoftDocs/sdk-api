---
UID: NN:wsdhost.IWSDDeviceHost
title: IWSDDeviceHost (wsdhost.h)
description: Represents a DPWS-compliant device.
helpviewer_keywords: ["IWSDDeviceHost","IWSDDeviceHost interface","IWSDDeviceHost interface","described","ncd.iwsddevicehost","wsdhost/IWSDDeviceHost"]
old-location: ncd\iwsddevicehost.htm
tech.root: ncd
ms.assetid: 497d0331-c88d-4381-8990-94227a9b9659
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost, IWSDDeviceHost interface, IWSDDeviceHost interface,described, ncd.iwsddevicehost, wsdhost/IWSDDeviceHost
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDDeviceHost
 - wsdhost/IWSDDeviceHost
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost
---

# IWSDDeviceHost interface


## -description

Represents a DPWS-compliant device . The device host will announce its presence on the network using the WS-Discovery protocol. The device host will also automatically respond to discovery queries and metadata requests.

The caller can register user-implemented services with the device host. These services will be exposed in the device metadata and the services will be available over the network. Messages bound for these services will be automatically dispatched into the service object.

Call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-wsdcreatedevicehost">WSDCreateDeviceHost</a> or <a href="/windows/desktop/api/wsdhost/nf-wsdhost-wsdcreatedevicehostadvanced">WSDCreateDeviceHostAdvanced</a> to create an object that exposes this interface.

## -inheritance

The <b>IWSDDeviceHost</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDDeviceHost</b> also has these types of members:

## -remarks

After retrieving this interface, the application would then:

<ol>
<li>Call the <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerporttype">RegisterPortType</a> method to register all necessary port types.</li>
<li>Call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-setmetadata">SetMetadata</a> to describe the device and optionally call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">RegisterService</a> one or more times to register services described in the service host metadata.</li>
<li>Call the <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-start">Start</a> method to start the device host and to publish the device using WS-Discovery.After starting the device host, you can optionally:

<ol>
<li>Call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-adddynamicservice">AddDynamicService</a> for services not described in the service host metadata (for example, an ad hoc print job).</li>
<li>Call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-retireservice">RetireService</a> to terminate action on and disconnect a service activated by the <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">RegisterService</a> method.</li>
<li>Call the <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-signalevent">SignalEvent</a> method to indicate that notifications should be sent for subscriptions relating to a particular event.</li>
</ol>
</li>
<li>Call the <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-stop">Stop</a> method to terminate host execution and terminate publication of the device.</li>
</ol>


An <b>IWSDDeviceHost</b> object can provide an object for a service on demand (using a notification callback) when calling the host receives a request message directed at that service.

## -see-also

<a href="/windows/desktop/WsdApi/overview-of-the-wsdapi-interfaces">Overview of the WSDAPI Interfaces</a>
