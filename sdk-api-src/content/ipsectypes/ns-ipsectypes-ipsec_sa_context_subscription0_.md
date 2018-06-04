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

# IPSEC_SA_CONTEXT_SUBSCRIPTION0_ structure


## -description


The <b>IPSEC_SA_CONTEXT_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a particular IPsec security association (SA) context.


## -struct-fields




### -field enumTemplate

Type: <b><a href="https://msdn.microsoft.com/2e099545-4075-4ea0-9035-53ce334decc4">IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</a>*</b>

Enumeration template for limiting the subscription.


### -field flags

Type: <b>UINT32</b>

This member is reserved for system use.


### -field sessionKey

Type: <b>GUID</b>

Identifies the session that created the subscription.


## -see-also




<a href="https://msdn.microsoft.com/2e099545-4075-4ea0-9035-53ce334decc4">IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</a>
 

 

