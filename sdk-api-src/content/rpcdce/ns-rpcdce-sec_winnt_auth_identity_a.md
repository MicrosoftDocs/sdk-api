---
UID: NS:rpcdce._SEC_WINNT_AUTH_IDENTITY_A
title: SEC_WINNT_AUTH_IDENTITY_A (rpcdce.h)
description: The SEC_WINNT_AUTH_IDENTITY structure enables passing a particular user name and password to the run-time library for the purpose of authentication. The structure is valid for Windows and Macintosh. (ANSI)
helpviewer_keywords: ["*PSEC_WINNT_AUTH_IDENTITY","*PSEC_WINNT_AUTH_IDENTITY structure [RPC]","*PSEC_WINNT_AUTH_IDENTITY_A","SEC_WINNT_AUTH_IDENTITY","SEC_WINNT_AUTH_IDENTITY structure [RPC]","SEC_WINNT_AUTH_IDENTITY_A","SEC_WINNT_AUTH_IDENTITY_ANSI","SEC_WINNT_AUTH_IDENTITY_UNICODE","SEC_WINNT_AUTH_IDENTITY_W","_SEC_WINNT_AUTH_IDENTITY_A","_SEC_WINNT_AUTH_IDENTITY_W","_rpc_sec_winnt_auth_identity","rpc.sec_winnt_auth_identity","rpcdce/*PSEC_WINNT_AUTH_IDENTITY","rpcdce/SEC_WINNT_AUTH_IDENTITY"]
old-location: rpc\sec_winnt_auth_identity.htm
tech.root: Rpc
ms.assetid: 829dee24-aeeb-4191-b5fc-85970725f064
ms.date: 12/05/2018
ms.keywords: '*PSEC_WINNT_AUTH_IDENTITY, *PSEC_WINNT_AUTH_IDENTITY structure [RPC], *PSEC_WINNT_AUTH_IDENTITY_A, SEC_WINNT_AUTH_IDENTITY, SEC_WINNT_AUTH_IDENTITY structure [RPC], SEC_WINNT_AUTH_IDENTITY_A, SEC_WINNT_AUTH_IDENTITY_ANSI, SEC_WINNT_AUTH_IDENTITY_UNICODE, SEC_WINNT_AUTH_IDENTITY_W, _SEC_WINNT_AUTH_IDENTITY_A, _SEC_WINNT_AUTH_IDENTITY_W, _rpc_sec_winnt_auth_identity, rpc.sec_winnt_auth_identity, rpcdce/*PSEC_WINNT_AUTH_IDENTITY, rpcdce/SEC_WINNT_AUTH_IDENTITY'
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SEC_WINNT_AUTH_IDENTITY_A, *PSEC_WINNT_AUTH_IDENTITY_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_WINNT_AUTH_IDENTITY_A
 - rpcdce/_SEC_WINNT_AUTH_IDENTITY_A
 - PSEC_WINNT_AUTH_IDENTITY_A
 - rpcdce/PSEC_WINNT_AUTH_IDENTITY_A
 - SEC_WINNT_AUTH_IDENTITY_A
 - rpcdce/SEC_WINNT_AUTH_IDENTITY_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - SEC_WINNT_AUTH_IDENTITY
 - SEC_WINNT_AUTH_IDENTITY_A
 - SEC_WINNT_AUTH_IDENTITY_W
---

# SEC_WINNT_AUTH_IDENTITY_A structure


## -description

The 
<b>SEC_WINNT_AUTH_IDENTITY</b> structure enables passing a particular user name and password to the run-time library for the purpose of authentication. The structure is valid for Windows and Macintosh.

## -struct-fields

### -field User

String containing the user name.

### -field UserLength

Number of characters in <b>User</b>, excluding the terminating <b>NULL</b>.

### -field Domain

String containing the domain  or workgroup name.

### -field DomainLength

Number of characters in <b>Domain</b>, excluding the terminating <b>NULL</b>.

### -field Password

String containing the user's password in the domain or workgroup.

### -field PasswordLength

Number of characters in <b>Password</b>, excluding the terminating <b>NULL</b>.

### -field Flags

Flags used to specify ANSI or UNICODE. Must be one of the following:

<a id="SEC_WINNT_AUTH_IDENTITY_ANSI"></a>
<a id="sec_winnt_auth_identity_ansi"></a>


#### SEC_WINNT_AUTH_IDENTITY_ANSI

<a id="SEC_WINNT_AUTH_IDENTITY_UNICODE"></a>
<a id="sec_winnt_auth_identity_unicode"></a>


#### SEC_WINNT_AUTH_IDENTITY_UNICODE

## -remarks

This structure must remain valid for the lifetime of the binding handle unless pointed to from the <a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_http_transport_credentials_a">RPC_HTTP_TRANSPORT_CREDENTIALS</a> or <a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a">RPC_HTTP_TRANSPORT_CREDENTIALS_V2</a> structure.

The strings may be ANSI or UNICODE depending on the value assigned to <b>Flags</b>.
