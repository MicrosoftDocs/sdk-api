---
UID: NS:wsdtypes._WSD_EVENTING_DELIVERY_MODE
title: "_WSD_EVENTING_DELIVERY_MODE"
author: windows-sdk-content
description: Represents the delivery mode used in a WS-Eventing Subscribe message.
old-location: ncd\wsd_eventing_delivery_mode.htm
old-project: wsdapi
ms.assetid: 6c767642-3b3c-47cb-afd9-c4c005241996
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSD_EVENTING_DELIVERY_MODE, WSD_EVENTING_DELIVERY_MODE structure, _WSD_EVENTING_DELIVERY_MODE, http://schemas.xmlsoap.org/ws/2004/08/eventing/DeliveryModes/Push, ncd.wsd_eventing_delivery_mode, wsdtypes/WSD_EVENTING_DELIVERY_MODE
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSD_EVENTING_DELIVERY_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_EVENTING_DELIVERY_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_EVENTING_DELIVERY_MODE structure


## -description


Represents the delivery mode  used in a WS-Eventing Subscribe message.


## -struct-fields




### -field Mode

Specifies the delivery mode for event delivery.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2004_08_eventing_DeliveryModes_Push"></a><a id="http___schemas.xmlsoap.org_ws_2004_08_eventing_deliverymodes_push"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2004_08_EVENTING_DELIVERYMODES_PUSH"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2004/08/eventing/DeliveryModes/Push</b></dt>
</dl>
</td>
<td width="60%">
Push mode delivery is used.

</td>
</tr>
</table>
 


### -field Push

 


### -field Data

A reference to the endpoint used for event delivery.  

