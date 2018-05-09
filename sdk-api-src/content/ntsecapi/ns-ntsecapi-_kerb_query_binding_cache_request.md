---
UID: NS:ntsecapi._KERB_QUERY_BINDING_CACHE_REQUEST
title: "_KERB_QUERY_BINDING_CACHE_REQUEST"
author: windows-driver-content
description: Contains information used to query the binding cache.
old-location: security\kerb_query_binding_cache_request.htm
old-project: SecAuthN
ms.assetid: 45DAA909-8D5D-4522-803B-E42EA8E09CE8
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PKERB_QUERY_BINDING_CACHE_REQUEST, KERB_QUERY_BINDING_CACHE_REQUEST, KERB_QUERY_BINDING_CACHE_REQUEST structure [Security], PKERB_QUERY_BINDING_CACHE_REQUEST, PKERB_QUERY_BINDING_CACHE_REQUEST structure pointer [Security], _KERB_QUERY_BINDING_CACHE_REQUEST, ntsecapi/KERB_QUERY_BINDING_CACHE_REQUEST, ntsecapi/PKERB_QUERY_BINDING_CACHE_REQUEST, security.kerb_query_binding_cache_request"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KERB_QUERY_BINDING_CACHE_REQUEST, *PKERB_QUERY_BINDING_CACHE_REQUEST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	KERB_QUERY_BINDING_CACHE_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _KERB_QUERY_BINDING_CACHE_REQUEST structure


## -description


Contains information used to query the binding cache. You must have the <b>SeTcbPrivilege</b> privilege set.


## -struct-fields




### -field MessageType

A 
						value of the <a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> authentication package by calling 
the <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbQueryBindingCacheMessage</b>.

