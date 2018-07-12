---
UID: NS:wsdtypes.__unnamed_struct_2
title: RESPONSEBODY_Subscribe
author: windows-sdk-content
description: Represents a WS-Eventing Subscribe response message.
old-location: ncd\responsebody_subscribe_struct.htm
old-project: wsdapi
ms.assetid: 8cba3835-9695-4741-b5ac-faba11c1c974
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: RESPONSEBODY_Subscribe, RESPONSEBODY_Subscribe structure, ncd.responsebody_subscribe_struct, wsdtypes/RESPONSEBODY_Subscribe
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
req.typenames: RESPONSEBODY_Subscribe
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - RESPONSEBODY_Subscribe
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RESPONSEBODY_Subscribe structure


## -description


Represents a WS-Eventing Subscribe response message.


## -struct-fields




### -field SubscriptionManager

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that represents the endpoint reference of the subscription manager.


### -field expires

Reference to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies when the subscription expires.


### -field any

 




#### - Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

