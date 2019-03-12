---
UID: NS:wsdtypes._WSD_EVENTING_DELIVERY_MODE_PUSH
title: WSD_EVENTING_DELIVERY_MODE_PUSH
author: windows-sdk-content
description: Represents the endpoint reference used for push delivery of events in a WS-Eventing Subscribe message.
old-location: ncd\wsd_eventing_delivery_mode_push.htm
tech.root: WsdApi
ms.assetid: 350d023f-18fb-4eb5-af47-81fdb54e594d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSD_EVENTING_DELIVERY_MODE_PUSH, WSD_EVENTING_DELIVERY_MODE_PUSH structure, ncd.wsd_eventing_delivery_mode_push, wsdtypes/WSD_EVENTING_DELIVERY_MODE_PUSH
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
 - WSD_EVENTING_DELIVERY_MODE_PUSH
product: Windows
targetos: Windows
req.typenames: WSD_EVENTING_DELIVERY_MODE_PUSH
req.redist: 
---

# WSD_EVENTING_DELIVERY_MODE_PUSH structure


## -description


Represents the endpoint reference  used for push delivery of events in a WS-Eventing Subscribe message.


## -struct-fields




### -field NotifyTo

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that specifies the endpoint reference to which notifications should be sent.

