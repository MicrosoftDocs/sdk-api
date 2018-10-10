---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT_SUBSCRIPTION0_
title: IPSEC_SA_CONTEXT_SUBSCRIPTION0_
author: windows-sdk-content
description: Stores information used to subscribe to notifications about a particular IPsec security association (SA) context.
old-location: fwp\ipsec_sa_context_subscription0.htm
tech.root: FWP
ms.assetid: d729f4e2-621a-4a39-beed-e339b76f53fc
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IPSEC_SA_CONTEXT_SUBSCRIPTION0, IPSEC_SA_CONTEXT_SUBSCRIPTION0 structure [Filtering], IPSEC_SA_CONTEXT_SUBSCRIPTION0_, fwp.ipsec_sa_context_subscription0, ipsectypes/IPSEC_SA_CONTEXT_SUBSCRIPTION0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_SA_CONTEXT_SUBSCRIPTION0
product: Windows
targetos: Windows
req.typenames: IPSEC_SA_CONTEXT_SUBSCRIPTION0
req.redist: 
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
 

 

