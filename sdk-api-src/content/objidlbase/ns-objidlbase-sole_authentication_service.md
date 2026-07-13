---
UID: NS:objidlbase.tagSOLE_AUTHENTICATION_SERVICE
title: SOLE_AUTHENTICATION_SERVICE (objidlbase.h)
description: The SOLE_AUTHENTICATION_SERVICE (objidlbase.h) structure identifies an authentication service that a server is willing to use to communicate to a client.
helpviewer_keywords: ["*PSOLE_AUTHENTICATION_SERVICE","PSOLE_AUTHENTICATION_SERVICE","PSOLE_AUTHENTICATION_SERVICE structure pointer [COM]","SOLE_AUTHENTICATION_SERVICE","SOLE_AUTHENTICATION_SERVICE structure [COM]","_com_SOLE_AUTHENTICATION_SERVICE","com.sole_authentication_service","objidlbase/PSOLE_AUTHENTICATION_SERVICE","objidlbase/SOLE_AUTHENTICATION_SERVICE","tagSOLE_AUTHENTICATION_SERVICE"]
old-location: com\sole_authentication_service.htm
tech.root: com
ms.assetid: 77fd15d7-54d4-4812-93d3-13a671e7afff
ms.date: 08/15/2022
ms.keywords: '*PSOLE_AUTHENTICATION_SERVICE, PSOLE_AUTHENTICATION_SERVICE, PSOLE_AUTHENTICATION_SERVICE structure pointer [COM], SOLE_AUTHENTICATION_SERVICE, SOLE_AUTHENTICATION_SERVICE structure [COM], _com_SOLE_AUTHENTICATION_SERVICE, com.sole_authentication_service, objidlbase/PSOLE_AUTHENTICATION_SERVICE, objidlbase/SOLE_AUTHENTICATION_SERVICE, tagSOLE_AUTHENTICATION_SERVICE'
req.header: objidlbase.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: SOLE_AUTHENTICATION_SERVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSOLE_AUTHENTICATION_SERVICE
 - objidlbase/tagSOLE_AUTHENTICATION_SERVICE
 - SOLE_AUTHENTICATION_SERVICE
 - objidlbase/SOLE_AUTHENTICATION_SERVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - SOLE_AUTHENTICATION_SERVICE
---

# SOLE_AUTHENTICATION_SERVICE structure


## -description

Identifies an authentication service that a server is willing to use to communicate to a client.

## -struct-fields

### -field dwAuthnSvc

The authentication service. This member can be a single value from the <a href="/windows/desktop/com/com-authentication-service-constants">Authentication Service Constants</a>.

### -field dwAuthzSvc

The authorization service. This member can be a single value from the <a href="/windows/desktop/com/com-authorization-constants">Authorization Constants</a>.

### -field pPrincipalName

The principal name to be used with the authentication service. If the principal name is <b>NULL</b>, the current user identifier is assumed. A <b>NULL</b> principal name is allowed for NTLMSSP, Kerberos, and Snego authentication services but may not work for other authentication services. For Schannel, this member must point to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the server's certificate; if it <b>NULL</b> and if a certificate for the current user does not exist, RPC_E_NO_GOOD_SECURITY_PACKAGES is returned.

### -field hr

When used in <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>, set on return to indicate the status of the call to register the authentication services.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices">CoQueryAuthenticationServices</a>
