---
UID: NS:wsdtypes.__unnamed_struct_1
title: REQUESTBODY_Subscribe
author: windows-sdk-content
description: Represents a WS-Eventing Subscribe request message.
old-location: ncd\requestbody_subscribe_struct.htm
old-project: wsdapi
ms.assetid: 28e7ee55-ad82-4ee6-9716-80951525ca96
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: REQUESTBODY_Subscribe, REQUESTBODY_Subscribe structure, ncd.requestbody_subscribe_struct, wsdtypes/REQUESTBODY_Subscribe
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.redist: 
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
req.typenames: REQUESTBODY_Subscribe
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - REQUESTBODY_Subscribe
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# REQUESTBODY_Subscribe structure


## -description


Represents a WS-Eventing Subscribe request message.


## -struct-fields




### -field EndTo

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that represents the endpoint reference of the event recipient.


### -field Delivery

Reference  to a <a href="https://msdn.microsoft.com/6c767642-3b3c-47cb-afd9-c4c005241996">WSD_EVENTING_DELIVERY_MODE</a> structure that specifies the delivery mode. Only push delivery is supported.


### -field Expires

Reference to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies when the subscription will expire.


### -field Filter

Reference to a <a href="https://msdn.microsoft.com/e702aca8-9784-4e51-988b-f4311573c700">WSD_EVENTING_FILTER</a> structure that specifies a boolean expression used for event filtering. 


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

