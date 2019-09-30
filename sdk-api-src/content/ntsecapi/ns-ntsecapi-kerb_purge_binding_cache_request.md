---
UID: NS:ntsecapi._KERB_PURGE_BINDING_CACHE_REQUEST
title: KERB_PURGE_BINDING_CACHE_REQUEST (ntsecapi.h)
author: windows-sdk-content
description: Deletes the request for the binding cache.
old-location: security\kerb_purge_binding_cache_request.htm
tech.root: SecAuthN
ms.assetid: E78F90D6-8425-480C-B997-35CC4E5612E7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PKERB_PURGE_BINDING_CACHE_REQUEST, KERB_PURGE_BINDING_CACHE_REQUEST, KERB_PURGE_BINDING_CACHE_REQUEST structure [Security], PKERB_PURGE_BINDING_CACHE_REQUEST, PKERB_PURGE_BINDING_CACHE_REQUEST structure pointer [Security], ntsecapi/KERB_PURGE_BINDING_CACHE_REQUEST, ntsecapi/PKERB_PURGE_BINDING_CACHE_REQUEST, security.kerb_purge_binding_cache_request'
ms.topic: struct
f1_keywords:
- ntsecapi/KERB_PURGE_BINDING_CACHE_REQUEST
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
- KERB_PURGE_BINDING_CACHE_REQUEST
targetos: Windows
req.typenames: KERB_PURGE_BINDING_CACHE_REQUEST, *PKERB_PURGE_BINDING_CACHE_REQUEST
req.redist: 
ms.custom: 19H1
---

# KERB_PURGE_BINDING_CACHE_REQUEST structure


## -description


Deletes the request for the binding cache. You must have the <b>SeTcbPrivilege</b> privilege set.


## -struct-fields




### -field MessageType

A 
						value of the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package by calling 
the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbPurgeBindingCacheMessage</b>.

