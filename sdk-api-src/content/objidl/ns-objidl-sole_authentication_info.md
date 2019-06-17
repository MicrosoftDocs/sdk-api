---
UID: NS:objidl.tagSOLE_AUTHENTICATION_INFO
title: SOLE_AUTHENTICATION_INFO (objidl.h)
author: windows-sdk-content
description: Identifies an authentication service, authorization service, and the authentication information for the specified authentication service.
old-location: com\sole_authentication_info.htm
tech.root: com
ms.assetid: 23beb1b1-e4b7-4282-9868-5caf40a69a61
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSOLE_AUTHENTICATION_INFO, PSOLE_AUTHENTICATION_INFO, PSOLE_AUTHENTICATION_INFO structure pointer [COM], SOLE_AUTHENTICATION_INFO, SOLE_AUTHENTICATION_INFO structure [COM], _com_SOLE_AUTHENTICATION_INFO, com.sole_authentication_info, objidlbase/PSOLE_AUTHENTICATION_INFO, objidlbase/SOLE_AUTHENTICATION_INFO, tagSOLE_AUTHENTICATION_INFO"
ms.topic: struct
f1_keywords: ["objidl/SOLE_AUTHENTICATION_INFO"]
req.header: objidl.h
req.include-header: Objidl.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - SOLE_AUTHENTICATION_INFO
product: Windows
targetos: Windows
req.typenames: SOLE_AUTHENTICATION_INFO, *PSOLE_AUTHENTICATION_INFO
req.redist: 
ms.custom: 19H1
---

# SOLE_AUTHENTICATION_INFO structure


## -description


Identifies an authentication service, authorization service, and the authentication information for the specified authentication service.


## -struct-fields




### -field dwAuthnSvc

The authentication service. This member can be a single value from the <a href="https://docs.microsoft.com/windows/desktop/com/com-authentication-service-constants">Authentication Service Constants</a>.


### -field dwAuthzSvc

The authorization service. This member can be a single value from the <a href="https://docs.microsoft.com/windows/desktop/com/com-authorization-constants">Authorization Constants</a>.


### -field pAuthInfo

A pointer to the authentication information, whose type is specific to the authentication service identified by <b>dwAuthnSvc</b>.

For Schannel (<a href="https://docs.microsoft.com/windows/desktop/com/com-authentication-service-constants">RPC_C_AUTHN_GSS_SCHANNEL</a>), this member either points to a <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context">CERT_CONTEXT</a> structure that contains the client's X.509 certificate or is <b>NULL</b> if the client has no certificate or wishes to remain anonymous to the server.

For NTLMSSP (<a href="https://docs.microsoft.com/windows/desktop/com/com-authentication-service-constants">RPC_C_AUTHN_WINNT</a>) and Kerberos (RPC_C_AUTHN_GSS_KERBEROS), this member points to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa">SEC_WINNT_AUTH_IDENTITY_EX</a> structure that contains the user name and password.

For Snego (<a href="https://docs.microsoft.com/windows/desktop/com/com-authentication-service-constants">RPC_C_AUTHN_GSS_NEGOTIATE</a>), this member is either <b>NULL</b>, points to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure, or points to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. If it is <b>NULL</b>, Snego will pick a list of authentication services based on those available on the client computer. If it points to a <b>SEC_WINNT_AUTH_IDENTITY_EX</b> structure, the structure's <b>PackageList</b> member must point to a string containing a comma-separated list of authentication service names and the <b>PackageListLength</b> member must give the number of bytes in the <b>PackageList</b> string. If <b>PackageList</b> is <b>NULL</b>, all calls using Snego will fail.

For authentication services not registered with DCOM, <b>pAuthInfo</b> must be set to <b>NULL</b> and DCOM will use the process identity to represent the client. For more information, see <a href="https://docs.microsoft.com/windows/desktop/com/com-and-security-packages">COM and Security Packages</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagsole_authentication_list">SOLE_AUTHENTICATION_LIST</a>
 

 

