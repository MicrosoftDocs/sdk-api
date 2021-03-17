---
UID: NS:ntsecapi._KERB_ADD_CREDENTIALS_REQUEST_EX
title: KERB_ADD_CREDENTIALS_REQUEST_EX (ntsecapi.h)
description: Specifies a message to add, remove, or replace an extra server credential for a logon session, and the service principal names (SPNs) to be associated with that credential.
helpviewer_keywords: ["*PKERB_ADD_CREDENTIALS_REQUEST_EX","KERB_ADD_CREDENTIALS_REQUEST_EX","KERB_ADD_CREDENTIALS_REQUEST_EX structure [Security]","PKERB_ADD_CREDENTIALS_REQUEST_EX","PKERB_ADD_CREDENTIALS_REQUEST_EX structure pointer [Security]","ntsecapi/KERB_ADD_CREDENTIALS_REQUEST_EX","ntsecapi/PKERB_ADD_CREDENTIALS_REQUEST_EX","security.kerb_add_credentials_request_ex"]
old-location: security\kerb_add_credentials_request_ex.htm
tech.root: security
ms.assetid: 9e806fce-9b3e-4bc9-bd75-a692f0ca5680
ms.date: 12/05/2018
ms.keywords: '*PKERB_ADD_CREDENTIALS_REQUEST_EX, KERB_ADD_CREDENTIALS_REQUEST_EX, KERB_ADD_CREDENTIALS_REQUEST_EX structure [Security], PKERB_ADD_CREDENTIALS_REQUEST_EX, PKERB_ADD_CREDENTIALS_REQUEST_EX structure pointer [Security], ntsecapi/KERB_ADD_CREDENTIALS_REQUEST_EX, ntsecapi/PKERB_ADD_CREDENTIALS_REQUEST_EX, security.kerb_add_credentials_request_ex'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: KERB_ADD_CREDENTIALS_REQUEST_EX, *PKERB_ADD_CREDENTIALS_REQUEST_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_ADD_CREDENTIALS_REQUEST_EX
 - ntsecapi/_KERB_ADD_CREDENTIALS_REQUEST_EX
 - PKERB_ADD_CREDENTIALS_REQUEST_EX
 - ntsecapi/PKERB_ADD_CREDENTIALS_REQUEST_EX
 - KERB_ADD_CREDENTIALS_REQUEST_EX
 - ntsecapi/KERB_ADD_CREDENTIALS_REQUEST_EX
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
 - KERB_ADD_CREDENTIALS_REQUEST_EX
---

# KERB_ADD_CREDENTIALS_REQUEST_EX structure


## -description

Specifies a  message to add, remove, or replace an extra server credential for a logon session, and 
the <a href="/windows/desktop/SecGloss/s-gly">service principal names</a> (SPNs) to be associated with that 
credential. The <b>SeTcbPrivilege</b> constant is required to alter another logon account's credentials.

## -struct-fields

### -field Credentials

A <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_add_credentials_request">KERB_ADD_CREDENTIALS_REQUEST</a> structure that specifies the credentials to add, remove, or replace.

### -field PrincipalNameCount

The number of elements in the <b>PrincipalNames</b> array.

### -field PrincipalNames

An array of SPNs to be associated with the user account specified by the <b>Credentials</b> member

## -remarks

Calling the   <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function with this structure affects only the behavior of the <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (Kerberos)</a> function. Using this structure allows multiple physical and virtual servers to share a single identity.

## -see-also

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_add_credentials_request">KERB_ADD_CREDENTIALS_REQUEST</a>