---
UID: NS:mi._MI_UserCredentials
title: MI_UserCredentials (mi.h)
description: A user's credentials. It includes an authentication type and either a username and password or a certificate thumbprint.
helpviewer_keywords: ["MI_AUTH_TYPE_BASIC","MI_AUTH_TYPE_CLIENT_CERTS","MI_AUTH_TYPE_CREDSSP","MI_AUTH_TYPE_DEFAULT","MI_AUTH_TYPE_DIGEST","MI_AUTH_TYPE_ISSUER_CERT","MI_AUTH_TYPE_KERBEROS","MI_AUTH_TYPE_NEGO_NO_CREDS","MI_AUTH_TYPE_NEGO_WITH_CREDS","MI_AUTH_TYPE_NONE","MI_AUTH_TYPE_NTLM","MI_UserCredentials","MI_UserCredentials structure [Windows Management Infrastructure (MI)]","mi/MI_UserCredentials","wmi._mi_usercredentials","wmi_v2.mi_usercredentials"]
old-location: wmi_v2\mi_usercredentials.htm
tech.root: wmi_v2
ms.assetid: 30191cd1-00de-42ef-ac95-5e174d273c80
ms.date: 12/05/2018
ms.keywords: MI_AUTH_TYPE_BASIC, MI_AUTH_TYPE_CLIENT_CERTS, MI_AUTH_TYPE_CREDSSP, MI_AUTH_TYPE_DEFAULT, MI_AUTH_TYPE_DIGEST, MI_AUTH_TYPE_ISSUER_CERT, MI_AUTH_TYPE_KERBEROS, MI_AUTH_TYPE_NEGO_NO_CREDS, MI_AUTH_TYPE_NEGO_WITH_CREDS, MI_AUTH_TYPE_NONE, MI_AUTH_TYPE_NTLM, MI_UserCredentials, MI_UserCredentials structure [Windows Management Infrastructure (MI)], mi/MI_UserCredentials, wmi._mi_usercredentials, wmi_v2.mi_usercredentials
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_UserCredentials
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_UserCredentials
 - mi/_MI_UserCredentials
 - MI_UserCredentials
 - mi/MI_UserCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_UserCredentials
---

# MI_UserCredentials structure


## -description

A user's credentials.  It includes an authentication type and either a username
and password or a certificate thumbprint.

## -struct-fields

### -field authenticationType

#### MI_AUTH_TYPE_DEFAULT (MI_T("Default"))

Transport picks the default specific to it. For example, <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a> (winrm) uses Kerberos and NegotiateWithoutCredentials as default.



#### MI_AUTH_TYPE_NONE (MI_T("None"))

Do not authenticate, most servers require some kind of authentication.



#### MI_AUTH_TYPE_DIGEST (MI_T("Digest"))

Uses Digest authentication. Requires username/password. Some servers and transports do not support this type of authentication.



#### MI_AUTH_TYPE_NEGO_WITH_CREDS (MI_T("NegoWithCreds"))

Uses SPNEGO authentication. Requires username/password.



#### MI_AUTH_TYPE_NEGO_NO_CREDS (MI_T("NegoNoCreds"))

Uses SPNEGO authentication with the current thread ID (or the process token, if no thread token exists).



#### MI_AUTH_TYPE_BASIC (MI_T("Basic"))

Uses basic authentication. Requires username/password. Some transports do not support this type of authentication. This authentication type is not very secure.



#### MI_AUTH_TYPE_KERBEROS (MI_T("Kerberos"))

Username/password optional.



#### MI_AUTH_TYPE_CLIENT_CERTS (MI_T("ClientCerts"))

Requires certificate thumbprint.



#### MI_AUTH_TYPE_NTLM (MI_T("Ntlmdomain"))

Username/password optional.



#### MI_AUTH_TYPE_CREDSSP (MI_T("CredSSP"))

Uses CREDSSP, a delegated authentication mechanism. Username/password are optional. Some transports support this authentication type. Configuration is required on both the client and the server to enable CREDSSP.



#### MI_AUTH_TYPE_ISSUER_CERT (MI_T("IssuerCert"))

Push/Source Initiated subscriptions only.

### -field credentials

### -field credentials.usernamePassword

Contains username and password information.

### -field credentials.certificateThumbprint

Certificate thumbprint for the user.