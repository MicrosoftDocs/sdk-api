---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT_SUBSCRIPTION0_
title: IPSEC_SA_CONTEXT_SUBSCRIPTION0 (ipsectypes.h)
author: windows-sdk-content
description: Stores information used to subscribe to notifications about a particular IPsec security association (SA) context.
old-location: fwp\ipsec_sa_context_subscription0.htm
tech.root: fwp
ms.assetid: d729f4e2-621a-4a39-beed-e339b76f53fc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_CONTEXT_SUBSCRIPTION0, IPSEC_SA_CONTEXT_SUBSCRIPTION0 structure [Filtering], fwp.ipsec_sa_context_subscription0, ipsectypes/IPSEC_SA_CONTEXT_SUBSCRIPTION0
ms.topic: struct
f1_keywords: 
 - "ipsectypes/IPSEC_SA_CONTEXT_SUBSCRIPTION0"
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
ms.custom: 19H1
---

# IPSEC_SA_CONTEXT_SUBSCRIPTION0 structure


## -description


The <b>IPSEC_SA_CONTEXT_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a particular IPsec security association (SA) context.


## -struct-fields




### -field enumTemplate

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0">IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</a>*</b>

Enumeration template for limiting the subscription.


### -field flags

Type: <b>UINT32</b>

This member is reserved for system use.


### -field sessionKey

Type: <b>GUID</b>

Identifies the session that created the subscription.


## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0">IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</a>
 

 

