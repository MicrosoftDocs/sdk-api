---
UID: NS:authz._AUTHZ_RPC_INIT_INFO_CLIENT
title: AUTHZ_RPC_INIT_INFO_CLIENT (authz.h)
description: Initializes a remote resource manager for a client.
helpviewer_keywords: ["*PAUTHZ_RPC_INIT_INFO_CLIENT","AUTHZ_RPC_INIT_INFO_CLIENT","AUTHZ_RPC_INIT_INFO_CLIENT structure [Security]","PAUTHZ_RPC_INIT_INFO_CLIENT","PAUTHZ_RPC_INIT_INFO_CLIENT structure pointer [Security]","authz/AUTHZ_RPC_INIT_INFO_CLIENT","authz/PAUTHZ_RPC_INIT_INFO_CLIENT","security.authz_rpc_init_info_client"]
old-location: security\authz_rpc_init_info_client.htm
tech.root: security
ms.assetid: 6859A0CB-F88E-42BF-A350-293D28E908DD
ms.date: 12/05/2018
ms.keywords: '*PAUTHZ_RPC_INIT_INFO_CLIENT, AUTHZ_RPC_INIT_INFO_CLIENT, AUTHZ_RPC_INIT_INFO_CLIENT structure [Security], PAUTHZ_RPC_INIT_INFO_CLIENT, PAUTHZ_RPC_INIT_INFO_CLIENT structure pointer [Security], authz/AUTHZ_RPC_INIT_INFO_CLIENT, authz/PAUTHZ_RPC_INIT_INFO_CLIENT, security.authz_rpc_init_info_client'
req.header: authz.h
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
targetos: Windows
req.typenames: AUTHZ_RPC_INIT_INFO_CLIENT, *PAUTHZ_RPC_INIT_INFO_CLIENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUTHZ_RPC_INIT_INFO_CLIENT
 - authz/_AUTHZ_RPC_INIT_INFO_CLIENT
 - PAUTHZ_RPC_INIT_INFO_CLIENT
 - authz/PAUTHZ_RPC_INIT_INFO_CLIENT
 - AUTHZ_RPC_INIT_INFO_CLIENT
 - authz/AUTHZ_RPC_INIT_INFO_CLIENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_RPC_INIT_INFO_CLIENT
---

# AUTHZ_RPC_INIT_INFO_CLIENT structure


## -description

The <b>AUTHZ_RPC_INIT_INFO_CLIENT</b> structure initializes a remote resource manager for a client.

## -struct-fields

### -field version

Version of the structure. The highest currently supported version is AUTHZ_RPC_INIT_INFO_CLIENT_VERSION_V1.

### -field ObjectUuid

Null-terminated string representation of the resource manager UUID. Only the following values are valid.

<ul>
<li>Use “5fc860e0-6f6e-4fc2-83cd-46324f25e90b” for remote effective access evaluation that ignores central policy.</li>
<li>Use “9a81c2bd-a525-471d-a4ed-49907c0b23da” for remote effective access evaluation that takes central policy into account.</li>
</ul>

### -field ProtSeq

Null-terminated string representation of a protocol sequence. This can be the following value.

<ul>
<li>“ncacn_ip_tcp”.</li>
</ul>

### -field NetworkAddr

Null-terminated string representation of a network address. The network-address format is associated with the protocol sequence.

### -field Endpoint

Null-terminated string representation of an endpoint. The endpoint format and content are associated with the protocol sequence. For example, the endpoint associated with the protocol sequence <a href="/windows/desktop/Midl/ncacn-np">ncacn_np</a> is a pipe name in the format <b>\\</b><i>Pipe</i><b>\\</b><i>PipeName</i>.

### -field Options

Null-terminated string representation of network options. The option string is associated with the protocol sequence.

### -field ServerSpn

Server Principal Name (SPN) of the server. If this member is missing, it is constructed from <b>NetworkAddr</b> assuming "host" service class.

## -remarks

For a sample that uses this structure, see the [Effective access rights for files sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Security/EffectiveAccessRights).