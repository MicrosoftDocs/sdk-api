---
UID: NS:ntsecapi._KERB_QUERY_TKT_CACHE_RESPONSE
title: "_KERB_QUERY_TKT_CACHE_RESPONSE"
author: windows-sdk-content
description: Contains the results of querying the ticket cache.
old-location: security\kerb_query_tkt_cache_response.htm
tech.root: secauthn
ms.assetid: 2101c1de-f304-4d44-899f-f9f03cd50934
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PKERB_QUERY_TKT_CACHE_RESPONSE, KERB_QUERY_TKT_CACHE_RESPONSE, KERB_QUERY_TKT_CACHE_RESPONSE structure [Security], PKERB_QUERY_TKT_CACHE_RESPONSE, PKERB_QUERY_TKT_CACHE_RESPONSE structure pointer [Security], _KERB_QUERY_TKT_CACHE_RESPONSE, _lsa_kerb_query_tkt_cache_response, ntsecapi/KERB_QUERY_TKT_CACHE_RESPONSE, ntsecapi/PKERB_QUERY_TKT_CACHE_RESPONSE, security.kerb_query_tkt_cache_response"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - KERB_QUERY_TKT_CACHE_RESPONSE
product: Windows
targetos: Windows
req.typenames: KERB_QUERY_TKT_CACHE_RESPONSE, *PKERB_QUERY_TKT_CACHE_RESPONSE
req.redist: 
---

# _KERB_QUERY_TKT_CACHE_RESPONSE structure


## -description


The <b>KERB_QUERY_TKT_CACHE_RESPONSE</b> structure contains the results of querying the ticket cache.

It is used by 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member must be set to <b>KerbQueryTicketCacheMessage</b>.


### -field CountOfTickets

Number of tickets in <b>Tickets</b> array. This can be zero if no tickets are available for the specified logon session.


### -field Tickets

Array of length <b>CountOfTickets</b> of 
<a href="https://msdn.microsoft.com/e9ac70f0-65dc-4c5a-b41f-7c4659680333">KERB_TICKET_CACHE_INFO</a> structures.


## -remarks



This buffer is allocated by the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> authentication package and should be deleted by the application that called <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>, using 
<a href="https://msdn.microsoft.com/e814ed68-07e7-4936-ba96-5411086f43f6">LsaFreeReturnBuffer</a>.



