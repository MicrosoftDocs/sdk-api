---
UID: NN:upnp.IUPnPDeviceFinderAddCallbackWithInterface
title: IUPnPDeviceFinderAddCallbackWithInterface
author: windows-sdk-content
description: The IUPnPDeviceFinderAddCallbackWithInterface interface allows the UPnP framework to communicate to an application:\_

The devices found during an asynchronous search.
The network interface through which the device advertisement came.

The IUPnPDeviceFinderAddCallbackWithInterface interface allows the UPnP framework to communicate to an application:
old-location: upnp\iupnpdevicefinderaddcallbackwithinterface.htm
tech.root: UPnP
ms.assetid: b0d78121-35d0-4f33-b1e9-19e0b2c5b78f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUPnPDeviceFinderAddCallbackWithInterface, IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs], IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs],described, upnp.iupnpdevicefinderaddcallbackwithinterface, upnp/IUPnPDeviceFinderAddCallbackWithInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinderAddCallbackWithInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDeviceFinderAddCallbackWithInterface interface


## -description



The <b>IUPnPDeviceFinderAddCallbackWithInterface</b> interface allows the UPnP framework to communicate to an application:

<ul>
<li>The devices found during an asynchronous search.</li>
<li>The network interface through which the device advertisement came.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceFinderAddCallbackWithInterface</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPDeviceFinderAddCallbackWithInterface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceFinderAddCallbackWithInterface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7cd47e8-264b-4d1a-aed3-daf5801c240c">DeviceAddedWithInterface</a>
</td>
<td align="left" width="63%">
Invoked by the UPnP framework to notify the application that  a device has been added to the network.

</td>
</tr>
</table> 


## -remarks



If you implement this interface, you must also implement the <a href="https://msdn.microsoft.com/02f1220b-d400-469e-8a28-64871f7fcbe2">IUPnPDeviceFinderCallback</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/02f1220b-d400-469e-8a28-64871f7fcbe2">IUPnPDeviceFinderCallback</a>
 

 

