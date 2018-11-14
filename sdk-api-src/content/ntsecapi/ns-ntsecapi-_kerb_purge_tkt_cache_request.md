---
UID: NS:ntsecapi._KERB_PURGE_TKT_CACHE_REQUEST
title: "_KERB_PURGE_TKT_CACHE_REQUEST"
author: windows-sdk-content
description: Contains information used to delete entries from the ticket cache.
old-location: security\kerb_purge_tkt_cache_request.htm
tech.root: secauthn
ms.assetid: 4e5e944a-8163-42de-b534-3b0478d9f334
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PKERB_PURGE_TKT_CACHE_REQUEST, KERB_PURGE_TKT_CACHE_REQUEST, KERB_PURGE_TKT_CACHE_REQUEST structure [Security], PKERB_PURGE_TKT_CACHE_REQUEST, PKERB_PURGE_TKT_CACHE_REQUEST structure pointer [Security], _KERB_PURGE_TKT_CACHE_REQUEST, _lsa_kerb_purge_tkt_cache_request, ntsecapi/KERB_PURGE_TKT_CACHE_REQUEST, ntsecapi/PKERB_PURGE_TKT_CACHE_REQUEST, security.kerb_purge_tkt_cache_request"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - KERB_PURGE_TKT_CACHE_REQUEST
product: Windows
targetos: Windows
req.typenames: KERB_PURGE_TKT_CACHE_REQUEST, *PKERB_PURGE_TKT_CACHE_REQUEST
req.redist: 
---

# _KERB_PURGE_TKT_CACHE_REQUEST structure


## -description


The <b>KERB_PURGE_TKT_CACHE_REQUEST</b> structure contains information used to delete entries from the ticket cache.

It is used by 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member must be set to <b>KerbPurgeTicketCacheMessage</b>.


### -field LogonId


<a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> structure containing the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a> identifier. This can be zero for the current user's logon session. If not zero, the caller must have the SeTcbPrivilege privilege set. If this fails, the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> authentication package sets the <i>ProtocolStatus</i> parameter of <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> to <b>STATUS_ACCESS_DENIED</b>.


### -field ServerName


<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> containing the name of the service whose tickets should be deleted from the cache.


### -field RealmName


<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> containing the name of the realm whose tickets should be deleted from the cache.


## -remarks



If both <b>ServerName</b> and <b>RealmName</b> are of zero length, <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> will delete all tickets for the logon session identified by <b>LogonId</b>. Otherwise, <b>LsaCallAuthenticationPackage</b> will search the cache tickets for <b>ServerName</b>@<b>RealmName</b>, and will delete all such tickets.


<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> does not return this buffer. It returns STATUS_SUCCESS if one or more tickets are deleted. If no tickets are found, the function returns SEC_E_NO_CREDENTIALS.



