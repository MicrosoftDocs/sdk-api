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

# IPSEC_SA_CONTEXT_CHANGE0_ structure


## -description


The <b>IPSEC_SA_CONTEXT_CHANGE0</b> structure contains information about an IPsec security association (SA) context  change.


## -struct-fields




### -field changeType

Type: <b><a href="https://msdn.microsoft.com/3e179d08-2962-4196-9c7e-c16c9cddf489">IPSEC_SA_CONTEXT_EVENT_TYPE0</a></b>

The type of IPsec SA context change event.


### -field saContextId

Type: <b>UINT64</b>

Identifier of the IPsec SA context that changed.


## -see-also




<a href="https://msdn.microsoft.com/3e179d08-2962-4196-9c7e-c16c9cddf489">IPSEC_SA_CONTEXT_EVENT_TYPE0</a>
 

 

