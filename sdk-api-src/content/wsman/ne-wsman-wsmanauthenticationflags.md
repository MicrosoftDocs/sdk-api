---
UID: NE:wsman.WSManAuthenticationFlags
title: WSManAuthenticationFlags (wsman.h)
description: Determines the authentication method for the operation.
helpviewer_keywords: ["WSMAN_FLAG_AUTH_BASIC","WSMAN_FLAG_AUTH_CLIENT_CERTIFICATE","WSMAN_FLAG_AUTH_CREDSSP","WSMAN_FLAG_AUTH_DIGEST","WSMAN_FLAG_AUTH_KERBEROS","WSMAN_FLAG_AUTH_NEGOTIATE","WSMAN_FLAG_DEFAULT_AUTHENTICATION","WSMAN_FLAG_NO_AUTHENTICATION","WSManAuthenticationFlags","WSManAuthenticationFlags enumeration [Windows Remote Management]","winrm.wsmanauthenticationflags","wsman/WSMAN_FLAG_AUTH_BASIC","wsman/WSMAN_FLAG_AUTH_CLIENT_CERTIFICATE","wsman/WSMAN_FLAG_AUTH_CREDSSP","wsman/WSMAN_FLAG_AUTH_DIGEST","wsman/WSMAN_FLAG_AUTH_KERBEROS","wsman/WSMAN_FLAG_AUTH_NEGOTIATE","wsman/WSMAN_FLAG_DEFAULT_AUTHENTICATION","wsman/WSMAN_FLAG_NO_AUTHENTICATION","wsman/WSManAuthenticationFlags"]
old-location: winrm\wsmanauthenticationflags.htm
tech.root: winrm
ms.assetid: ce5ddaf6-4d81-4dab-a928-819b1fdee6c8
ms.date: 12/05/2018
ms.keywords: WSMAN_FLAG_AUTH_BASIC, WSMAN_FLAG_AUTH_CLIENT_CERTIFICATE, WSMAN_FLAG_AUTH_CREDSSP, WSMAN_FLAG_AUTH_DIGEST, WSMAN_FLAG_AUTH_KERBEROS, WSMAN_FLAG_AUTH_NEGOTIATE, WSMAN_FLAG_DEFAULT_AUTHENTICATION, WSMAN_FLAG_NO_AUTHENTICATION, WSManAuthenticationFlags, WSManAuthenticationFlags enumeration [Windows Remote Management], winrm.wsmanauthenticationflags, wsman/WSMAN_FLAG_AUTH_BASIC, wsman/WSMAN_FLAG_AUTH_CLIENT_CERTIFICATE, wsman/WSMAN_FLAG_AUTH_CREDSSP, wsman/WSMAN_FLAG_AUTH_DIGEST, wsman/WSMAN_FLAG_AUTH_KERBEROS, wsman/WSMAN_FLAG_AUTH_NEGOTIATE, wsman/WSMAN_FLAG_DEFAULT_AUTHENTICATION, wsman/WSMAN_FLAG_NO_AUTHENTICATION, wsman/WSManAuthenticationFlags
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManAuthenticationFlags
 - wsman/WSManAuthenticationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSManAuthenticationFlags
---

# WSManAuthenticationFlags enumeration


## -description

Determines the authentication method for the operation.

## -enum-fields

### -field WSMAN_FLAG_DEFAULT_AUTHENTICATION:0x0

Use the default authentication.

### -field WSMAN_FLAG_NO_AUTHENTICATION:0x1

Use no authentication for a remote operation.

### -field WSMAN_FLAG_AUTH_DIGEST:0x2

Use Digest authentication. Only the client computer can initiate a Digest authentication request. The client sends a request to the server to authenticate and receives from the server a token string. The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string. Digest authentication is supported for HTTP and HTTPS. WinRM Shell client scripts and applications can specify Digest authentication, but the service cannot.

### -field WSMAN_FLAG_AUTH_NEGOTIATE:0x4

Use Negotiate authentication. The client sends a request to the server to authenticate. The server determines whether to use Kerberos or NTLM. In general, Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts. But there are also some special cases in which Kerberos/NTLM are selected. The user name should be specified in the form DOMAIN\username for a domain user or SERVERNAME\username for a local user on a server computer.

### -field WSMAN_FLAG_AUTH_BASIC:0x8

Use Basic authentication. The client presents credentials in the form of a user name and password that are directly transmitted in the request message. You can specify the credentials only of  a local administrator account on the remote computer.

### -field WSMAN_FLAG_AUTH_KERBEROS:0x10

Use Kerberos authentication. The client and server mutually authenticate by using Kerberos certificates.

### -field WSMAN_FLAG_AUTH_CREDSSP:0x80

Use CredSSP authentication for a remote operation. If a certificate from the local machine is used to authenticate the server, the Network service must be allowed access to the private key of the certificate.

### -field WSMAN_FLAG_AUTH_CLIENT_CERTIFICATE:0x20     

Use client certificate authentication. The certificate thumbprint is passed as part of the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_authentication_credentials">WSMAN_AUTHENTICATION_CREDENTIALS</a> structure. The WinRM client will try to find the certificate in the computer store and then, if it is not found, in the current user store. If no matching certificate is found, an error will be reported to the user.
