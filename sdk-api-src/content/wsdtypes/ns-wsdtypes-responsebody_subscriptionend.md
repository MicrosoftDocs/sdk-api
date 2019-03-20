---
UID: NS:wsdtypes.__unnamed_struct_8
title: RESPONSEBODY_SubscriptionEnd (wsdtypes.h)
author: windows-sdk-content
description: Represents a WS-Eventing SubscriptionEnd response message.
old-location: ncd\responsebody_subscriptionend.htm
tech.root: WsdApi
ms.assetid: 84faf4b7-6bdc-4ecc-92c0-c27e36bbe912
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RESPONSEBODY_SubscriptionEnd, RESPONSEBODY_SubscriptionEnd structure, http://schemas.xmlsoap.org/ws/2004/08/eventing/DeliveryFailure, http://schemas.xmlsoap.org/ws/2004/08/eventing/SourceCancelling, http://schemas.xmlsoap.org/ws/2004/08/eventing/SourceShuttingDown, ncd.responsebody_subscriptionend, wsdtypes/RESPONSEBODY_SubscriptionEnd
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - RESPONSEBODY_SubscriptionEnd
product: Windows
targetos: Windows
req.typenames: RESPONSEBODY_SubscriptionEnd
req.redist: 
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

