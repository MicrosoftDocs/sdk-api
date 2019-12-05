---
UID: NS:wsdtypes.__unnamed_struct_1
title: REQUESTBODY_Subscribe (wsdtypes.h)
description: Represents a WS-Eventing Subscribe request message.
old-location: ncd\requestbody_subscribe_struct.htm
tech.root: WsdApi
ms.assetid: 28e7ee55-ad82-4ee6-9716-80951525ca96
ms.date: 12/05/2018
ms.keywords: REQUESTBODY_Subscribe, REQUESTBODY_Subscribe structure, ncd.requestbody_subscribe_struct, wsdtypes/REQUESTBODY_Subscribe
ms.topic: struct
f1_keywords:
- wsdtypes/REQUESTBODY_Subscribe
dev_langs:
- c++
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
- REQUESTBODY_Subscribe
targetos: Windows
req.typenames: REQUESTBODY_Subscribe
req.redist: 
ms.custom: 19H1
---

# REQUESTBODY_Subscribe structure


## -description


Represents a WS-Eventing Subscribe request message.


## -struct-fields




### -field EndTo

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that represents the endpoint reference of the event recipient.


### -field Delivery

Reference  to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_delivery_mode">WSD_EVENTING_DELIVERY_MODE</a> structure that specifies the delivery mode. Only push delivery is supported.


### -field Expires

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies when the subscription will expire.


### -field Filter

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_filter">WSD_EVENTING_FILTER</a> structure that specifies a boolean expression used for event filtering. 


### -field Any

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

