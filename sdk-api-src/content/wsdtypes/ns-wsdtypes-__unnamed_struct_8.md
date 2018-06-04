---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RESPONSEBODY_SubscriptionEnd structure


## -description


Represents a WS-Eventing SubscriptionEnd response message.


## -struct-fields




### -field SubscriptionManager

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that represents the endpoint reference of the subscription manager.


### -field Status

A string that describes the reason the subscription ended.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2004_08_eventing_SourceShuttingDown"></a><a id="http___schemas.xmlsoap.org_ws_2004_08_eventing_sourceshuttingdown"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2004_08_EVENTING_SOURCESHUTTINGDOWN"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2004/08/eventing/SourceShuttingDown</b></dt>
</dl>
</td>
<td width="60%">
The event source is shutting down.

</td>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2004_08_eventing_SourceCancelling"></a><a id="http___schemas.xmlsoap.org_ws_2004_08_eventing_sourcecancelling"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2004_08_EVENTING_SOURCECANCELLING"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2004/08/eventing/SourceCancelling</b></dt>
</dl>
</td>
<td width="60%">
The event source canceled the subscription for another reason.

</td>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2004_08_eventing_DeliveryFailure"></a><a id="http___schemas.xmlsoap.org_ws_2004_08_eventing_deliveryfailure"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2004_08_EVENTING_DELIVERYFAILURE"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2004/08/eventing/DeliveryFailure</b></dt>
</dl>
</td>
<td width="60%">
The event source ended the subscription because the delivery of notifications failed.

</td>
</tr>
</table>
 


### -field Reason

Reference to a  <a href="https://msdn.microsoft.com/c90cc459-a10d-4b2b-81bc-96e562755b6c">WSD_LOCALIZED_STRING</a> that contains a human-readable explanation of the reason the subscription ended. 


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

