---
UID: NS:wsdtypes.RESPONSEBODY_Subscribe
title: RESPONSEBODY_Subscribe (wsdtypes.h)
description: Represents a WS-Eventing Subscribe response message.
helpviewer_keywords: ["RESPONSEBODY_Subscribe","RESPONSEBODY_Subscribe structure","ncd.responsebody_subscribe_struct","wsdtypes/RESPONSEBODY_Subscribe"]
old-location: ncd\responsebody_subscribe_struct.htm
tech.root: ncd
ms.assetid: 8cba3835-9695-4741-b5ac-faba11c1c974
ms.date: 12/05/2018
ms.keywords: RESPONSEBODY_Subscribe, RESPONSEBODY_Subscribe structure, ncd.responsebody_subscribe_struct, wsdtypes/RESPONSEBODY_Subscribe
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
targetos: Windows
req.typenames: RESPONSEBODY_Subscribe
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESPONSEBODY_Subscribe
 - wsdtypes/RESPONSEBODY_Subscribe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - RESPONSEBODY_Subscribe
---

# RESPONSEBODY_Subscribe structure


## -description

Represents a WS-Eventing Subscribe response message.

## -struct-fields

### -field SubscriptionManager

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that represents the endpoint reference of the subscription manager.

### -field expires

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies when the subscription expires.

### -field any

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

