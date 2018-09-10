---
UID: NN:wsdclient.IWSDDeviceProxy
title: IWSDDeviceProxy
author: windows-sdk-content
description: Represents a remote Devices Profile for Web Services (DPWS) device for client applications and middleware.
old-location: ncd\iwsddeviceproxy.htm
tech.root: WsdApi
ms.assetid: a1a54ba0-241a-4c3d-8113-89c0f8171c40
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDDeviceProxy, IWSDDeviceProxy interface, IWSDDeviceProxy interface,described, ncd.iwsddeviceproxy, wsdclient/IWSDDeviceProxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDDeviceProxy interface


## -description


Represents a remote Devices Profile for Web Services (DPWS) device for client applications and middleware.

To get this interface, you can call <a href="https://msdn.microsoft.com/d432ae9a-cf34-4149-978c-637443a3824f">WSDCreateDeviceProxy</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDDeviceProxy</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDDeviceProxy</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a>
</td>
<td align="left" width="63%">
Sends an asynchronous request for metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a>
</td>
<td align="left" width="63%">
Ends an asynchronous request for metadata and returns the metadata related to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a0a3954-348f-4a9d-9e52-f72d29ec0425">GetAllMetadata</a>
</td>
<td align="left" width="63%">
Gets all metadata for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/088c14a7-f2aa-4415-a056-a0c725602938">GetEndpointProxy</a>
</td>
<td align="left" width="63%">
Gets the endpoint proxy for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1e81f75-baeb-4406-8de0-f575db573fe8">GetHostMetadata</a>
</td>
<td align="left" width="63%">
Gets class-specific metadata for the device describing the features of the device and the services it hosts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1c07b78-16f6-4595-8de3-0c6591096496">GetServiceProxyById</a>
</td>
<td align="left" width="63%">
Gets a generic <a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a> service proxy by service ID. Service IDs can be obtained by examining the service host metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20df9a62-b983-40ed-a4bc-07131b80de6e">GetServiceProxyByType</a>
</td>
<td align="left" width="63%">
Gets a generic <a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a> proxy for a service exposed by the device by port type name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95a87bb1-8e62-4ece-a7bc-2483ea282ede">GetThisDeviceMetadata</a>
</td>
<td align="left" width="63%">
Gets device-specific metadata for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a9343b8-34f3-41f9-8b02-853ae724ec75">GetThisModelMetadata</a>
</td>
<td align="left" width="63%">
Gets model-specific metadata for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d29212c8-2f29-41cc-ae35-8376ec5f0b7a">Init</a>
</td>
<td align="left" width="63%">
Initializes the device proxy, optionally sharing a session with a previously initialized sponsoring device proxy.

</td>
</tr>
</table> 


## -remarks



This interface is a client-side representation of a remote device. The proxy provides basic access to device metadata (<a href="https://msdn.microsoft.com/7b9d063f-f0d5-4333-a5d8-e9a6d2d9af88">WSD_THIS_DEVICE_METADATA</a> and <a href="https://msdn.microsoft.com/614daaeb-76ac-4dec-93fe-f413164d5330">WSD_THIS_MODEL_METADATA</a>), in addition to providing methods for creating service proxy objects. The service proxy objects correspond to service hosted on the device. For example, a television is a device and the tuner portion of the television is a service hosted on the device that has an accessible, atomic set of functions.

The <b>IWSDDeviceProxy</b> object exposes WSD-specific device semantics.

To use <b>IWSDDeviceProxy</b> in your client or middleware application: 



<ol>
<li>Call <a href="https://msdn.microsoft.com/d432ae9a-cf34-4149-978c-637443a3824f">WSDCreateDeviceProxy</a>.</li>
<li>Call any of the four metadata methods of the device proxy object.</li>
<li>Get an <a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a> object, either by calling <a href="https://msdn.microsoft.com/c1c07b78-16f6-4595-8de3-0c6591096496">GetServiceProxyById</a> or <a href="https://msdn.microsoft.com/20df9a62-b983-40ed-a4bc-07131b80de6e">GetServiceProxyByType</a>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/2b23d7d3-3b06-48c8-993e-49c72b139624">Overview of the WSDAPI Interfaces</a>
 

 

