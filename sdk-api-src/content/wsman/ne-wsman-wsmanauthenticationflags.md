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

# WSManAuthenticationFlags enumeration


## -description


Determines the authentication method for the operation.


## -enum-fields




### -field WSMAN_FLAG_DEFAULT_AUTHENTICATION

Use the default authentication.


### -field WSMAN_FLAG_NO_AUTHENTICATION

Use no authentication for a remote operation.


### -field WSMAN_FLAG_AUTH_DIGEST

Use Digest authentication. Only the client computer can initiate a Digest authentication request. The client sends a request to the server to authenticate and receives from the server a token string. The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string. Digest authentication is supported for HTTP and HTTPS. WinRM Shell client scripts and applications can specify Digest authentication, but the service cannot.


### -field WSMAN_FLAG_AUTH_NEGOTIATE

Use Negotiate authentication. The client sends a request to the server to authenticate. The server determines whether to use Kerberos or NTLM. In general, Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts. But there are also some special cases in which Kerberos/NTLM are selected. The user name should be specified in the form DOMAIN\username for a domain user or SERVERNAME\username for a local user on a server computer.


### -field WSMAN_FLAG_AUTH_BASIC

Use Basic authentication. The client presents credentials in the form of a user name and password that are directly transmitted in the request message. You can specify the credentials only of  a local administrator account on the remote computer.


### -field WSMAN_FLAG_AUTH_KERBEROS

Use Kerberos authentication. The client and server mutually authenticate by using Kerberos certificates.


### -field WSMAN_FLAG_AUTH_CREDSSP

Use CredSSP authentication for a remote operation. If a certificate from the local machine is used to authenticate the server, the Network service must be allowed access to the private key of the certificate.


### -field WSMAN_FLAG_AUTH_CLIENT_CERTIFICATE

Use client certificate authentication. The certificate thumbprint is passed as part of the <a href="https://msdn.microsoft.com/e9090d88-c76e-4a85-946e-ff46403e6725">WSMAN_AUTHENTICATION_CREDENTIALS</a> structure. The WinRM client will try to find the certificate in the computer store and then, if it is not found, in the current user store. If no matching certificate is found, an error will be reported to the user.

