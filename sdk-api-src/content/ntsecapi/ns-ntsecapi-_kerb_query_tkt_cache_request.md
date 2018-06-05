---
UID: NS:ntsecapi._KERB_QUERY_TKT_CACHE_REQUEST
title: "_KERB_QUERY_TKT_CACHE_REQUEST"
author: windows-sdk-content
description: Contains information used to query the ticket cache.
old-location: security\kerb_query_tkt_cache_request.htm
old-project: SecAuthN
ms.assetid: 3c8e63b3-9ac4-4228-87e1-6802c3d12d6c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PKERB_QUERY_TKT_CACHE_REQUEST, KERB_QUERY_TKT_CACHE_REQUEST, KERB_QUERY_TKT_CACHE_REQUEST structure [Security], PKERB_QUERY_TKT_CACHE_REQUEST, PKERB_QUERY_TKT_CACHE_REQUEST structure pointer [Security], _KERB_QUERY_TKT_CACHE_REQUEST, _lsa_kerb_query_tkt_cache_request, ntsecapi/KERB_QUERY_TKT_CACHE_REQUEST, ntsecapi/PKERB_QUERY_TKT_CACHE_REQUEST, security.kerb_query_tkt_cache_request"
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
tech.root: 
req.typenames: KERB_QUERY_TKT_CACHE_REQUEST, *PKERB_QUERY_TKT_CACHE_REQUEST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	KERB_QUERY_TKT_CACHE_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _KERB_QUERY_TKT_CACHE_REQUEST structure


## -description


The <b>KERB_QUERY_TKT_CACHE_REQUEST</b> structure contains information used to query the ticket cache.

It is used by 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member must be set to <b>KerbQueryTicketCacheMessage</b> or <b>KerbRetrieveTicketMessage</b>. 




If this member is set to <b>KerbQueryTicketCacheMessage</b>, the request is for information about all of the cached tickets for the specified user logon session. If it is set to <b>KerbRetrieveTicketMessage</b>, the request is for the ticket granting ticket from the ticket cache of the specified user logon session.


### -field LogonId


<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure containing the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a> identifier. This can be zero for the current user's logon session. If not zero, the caller must have the SeTcbPrivilege privilege set. If this fails, the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> authentication package sets the <i>ProtocolStatus</i> parameter of <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> to STATUS_ACCESS_DENIED.

