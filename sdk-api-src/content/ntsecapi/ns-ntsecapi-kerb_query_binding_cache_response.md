---
UID: NS:ntsecapi._KERB_QUERY_BINDING_CACHE_RESPONSE
title: KERB_QUERY_BINDING_CACHE_RESPONSE (ntsecapi.h)
author: windows-sdk-content
description: Contains the results of querying the binding cache.
old-location: security\kerb_query_binding_cache_response.htm
tech.root: SecAuthN
ms.assetid: D096068F-7EC0-4745-A361-142F9B478402
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PKERB_QUERY_BINDING_CACHE_RESPONSE, KERB_QUERY_BINDING_CACHE_RESPONSE, KERB_QUERY_BINDING_CACHE_RESPONSE structure [Security], PKERB_QUERY_BINDING_CACHE_RESPONSE, PKERB_QUERY_BINDING_CACHE_RESPONSE structure pointer [Security], ntsecapi/KERB_QUERY_BINDING_CACHE_RESPONSE, ntsecapi/PKERB_QUERY_BINDING_CACHE_RESPONSE, security.kerb_query_binding_cache_response"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_QUERY_BINDING_CACHE_RESPONSE
product: Windows
targetos: Windows
req.typenames: KERB_QUERY_BINDING_CACHE_RESPONSE, *PKERB_QUERY_BINDING_CACHE_RESPONSE
req.redist: 
ms.custom: 19H1
---

# KERB_QUERY_BINDING_CACHE_RESPONSE structure


## -description


Contains the results of querying the binding cache. You must have the <b>SeTcbPrivilege</b> privilege set.


## -struct-fields




### -field MessageType

A 
						value of the <a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> authentication package by calling 
the <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbQueryBindingCacheMessage</b>.


### -field CountOfEntries

The number of entries in the binding cache.


### -field Entries

 



