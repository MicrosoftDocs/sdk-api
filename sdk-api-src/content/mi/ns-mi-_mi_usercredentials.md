---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MI_UserCredentials structure


## -description


A user's credentials.  It includes an authentication type and either a username
and password or a certificate thumbprint.


## -struct-fields




### -field authenticationType



#### MI_AUTH_TYPE_DEFAULT (MI_T("Default"))

Transport picks the default specific to it. For example, <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a> (winrm) uses Kerberos and NegotiateWithoutCredentials as default.



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

