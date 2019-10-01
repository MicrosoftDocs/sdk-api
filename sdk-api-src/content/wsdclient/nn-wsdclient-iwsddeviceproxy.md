---
UID: NN:wsdclient.IWSDDeviceProxy
title: IWSDDeviceProxy (wsdclient.h)
author: windows-sdk-content
description: Represents a remote Devices Profile for Web Services (DPWS) device for client applications and middleware.
old-location: ncd\iwsddeviceproxy.htm
tech.root: WsdApi
ms.assetid: a1a54ba0-241a-4c3d-8113-89c0f8171c40
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDDeviceProxy, IWSDDeviceProxy interface, IWSDDeviceProxy interface,described, ncd.iwsddeviceproxy, wsdclient/IWSDDeviceProxy
ms.topic: interface
f1_keywords:
- wsdclient/IWSDDeviceProxy
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
- IWSDDeviceProxy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDDeviceProxy interface


## -description


Represents a remote Devices Profile for Web Services (DPWS) device for client applications and middleware.

To get this interface, you can call <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-wsdcreatedeviceproxy">WSDCreateDeviceProxy</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDDeviceProxy</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDDeviceProxy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDDeviceProxy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a>
</td>
<td align="left" width="63%">
Sends an asynchronous request for metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">EndGetMetadata</a>
</td>
<td align="left" width="63%">
Ends an asynchronous request for metadata and returns the metadata related to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getallmetadata">GetAllMetadata</a>
</td>
<td align="left" width="63%">
Gets all metadata for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getendpointproxy">GetEndpointProxy</a>
</td>
<td align="left" width="63%">
Gets the endpoint proxy for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-gethostmetadata">GetHostMetadata</a>
</td>
<td align="left" width="63%">
Gets class-specific metadata for the device describing the features of the device and the services it hosts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getserviceproxybyid">GetServiceProxyById</a>
</td>
<td align="left" width="63%">
Gets a generic <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> service proxy by service ID. Service IDs can be obtained by examining the service host metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getserviceproxybytype">GetServiceProxyByType</a>
</td>
<td align="left" width="63%">
Gets a generic <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> proxy for a service exposed by the device by port type name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getthisdevicemetadata">GetThisDeviceMetadata</a>
</td>
<td align="left" width="63%">
Gets device-specific metadata for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getthismodelmetadata">GetThisModelMetadata</a>
</td>
<td align="left" width="63%">
Gets model-specific metadata for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-init">Init</a>
</td>
<td align="left" width="63%">
Initializes the device proxy, optionally sharing a session with a previously initialized sponsoring device proxy.

</td>
</tr>
</table> 


## -remarks



This interface is a client-side representation of a remote device. The proxy provides basic access to device metadata (<a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_device_metadata">WSD_THIS_DEVICE_METADATA</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_model_metadata">WSD_THIS_MODEL_METADATA</a>), in addition to providing methods for creating service proxy objects. The service proxy objects correspond to service hosted on the device. For example, a television is a device and the tuner portion of the television is a service hosted on the device that has an accessible, atomic set of functions.

The <b>IWSDDeviceProxy</b> object exposes WSD-specific device semantics.

To use <b>IWSDDeviceProxy</b> in your client or middleware application: 



<ol>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-wsdcreatedeviceproxy">WSDCreateDeviceProxy</a>.</li>
<li>Call any of the four metadata methods of the device proxy object.</li>
<li>Get an <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> object, either by calling <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getserviceproxybyid">GetServiceProxyById</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getserviceproxybytype">GetServiceProxyByType</a>.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WsdApi/overview-of-the-wsdapi-interfaces">Overview of the WSDAPI Interfaces</a>
 

 

