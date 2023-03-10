---
UID: NS:ntsecapi._KERB_ADD_CREDENTIALS_REQUEST
title: KERB_ADD_CREDENTIALS_REQUEST (ntsecapi.h)
description: Specifies a message to add, remove, or replace an extra server credential for a logon session.
helpviewer_keywords: ["*PKERB_ADD_CREDENTIALS_REQUEST","KERB_ADD_CREDENTIALS_REQUEST","KERB_ADD_CREDENTIALS_REQUEST structure [Security]","KERB_REQUEST_ADD_CREDENTIAL","KERB_REQUEST_REMOVE_CREDENTIAL","KERB_REQUEST_REPLACE_CREDENTIAL","PKERB_ADD_CREDENTIALS_REQUEST","PKERB_ADD_CREDENTIALS_REQUEST structure pointer [Security]","ntsecapi/KERB_ADD_CREDENTIALS_REQUEST","ntsecapi/PKERB_ADD_CREDENTIALS_REQUEST","security.kerb_add_credentials_request"]
old-location: security\kerb_add_credentials_request.htm
tech.root: security
ms.assetid: a9a8810b-c9cf-4e19-8a33-7ad0c7ef8694
ms.date: 12/05/2018
ms.keywords: '*PKERB_ADD_CREDENTIALS_REQUEST, KERB_ADD_CREDENTIALS_REQUEST, KERB_ADD_CREDENTIALS_REQUEST structure [Security], KERB_REQUEST_ADD_CREDENTIAL, KERB_REQUEST_REMOVE_CREDENTIAL, KERB_REQUEST_REPLACE_CREDENTIAL, PKERB_ADD_CREDENTIALS_REQUEST, PKERB_ADD_CREDENTIALS_REQUEST structure pointer [Security], ntsecapi/KERB_ADD_CREDENTIALS_REQUEST, ntsecapi/PKERB_ADD_CREDENTIALS_REQUEST, security.kerb_add_credentials_request'
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
targetos: Windows
req.typenames: KERB_ADD_CREDENTIALS_REQUEST, *PKERB_ADD_CREDENTIALS_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_ADD_CREDENTIALS_REQUEST
 - ntsecapi/_KERB_ADD_CREDENTIALS_REQUEST
 - PKERB_ADD_CREDENTIALS_REQUEST
 - ntsecapi/PKERB_ADD_CREDENTIALS_REQUEST
 - KERB_ADD_CREDENTIALS_REQUEST
 - ntsecapi/KERB_ADD_CREDENTIALS_REQUEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_ADD_CREDENTIALS_REQUEST
---

# KERB_ADD_CREDENTIALS_REQUEST structure


## -description

Specifies a  message to add, remove, or replace an extra server credential for a logon session. The <b>SeTcbPrivilege</b> is required to alter another logon account's credentials.

## -struct-fields

### -field MessageType

A 
						value of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package by calling 
the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbAddExtraCredentialsMessage</b>.

### -field UserName

The user name for the credential.

### -field DomainName

The domain name for the credential.

### -field Password

The password for the credential.

### -field LogonId

The logon ID of the credential. The value of this member can be <b>NULL</b>.

### -field Flags

A value that specifies what to do with the credential. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_REQUEST_ADD_CREDENTIAL"></a><a id="kerb_request_add_credential"></a><dl>
<dt><b>KERB_REQUEST_ADD_CREDENTIAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Add the specified credential to the logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_REQUEST_REPLACE_CREDENTIAL"></a><a id="kerb_request_replace_credential"></a><dl>
<dt><b>KERB_REQUEST_REPLACE_CREDENTIAL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Replace the specified credential in the logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_REQUEST_REMOVE_CREDENTIAL"></a><a id="kerb_request_remove_credential"></a><dl>
<dt><b>KERB_REQUEST_REMOVE_CREDENTIAL</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Remove the specified credential from the logon session.

</td>
</tr>
</table>

## -remarks

Calling  the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function with this structure affects only the behavior of the <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (Kerberos)</a> function. Using this structure allows multiple physical and virtual servers to share a single identity.

## -see-also

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_add_credentials_request_ex">KERB_ADD_CREDENTIALS_REQUEST_EX</a>