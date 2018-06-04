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

# tagSOLE_AUTHENTICATION_SERVICE structure


## -description


Identifies an authentication service that a server is willing to use to communicate to a client.


## -struct-fields




### -field dwAuthnSvc

The authentication service. This member can be a single value from the <a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">Authentication Service Constants</a>.


### -field dwAuthzSvc

The authorization service. This member can be a single value from the <a href="https://msdn.microsoft.com/a0bc9337-b7e4-41c5-ae36-4843fa7d98ce">Authorization Constants</a>.


### -field pPrincipalName

The principal name to be used with the authentication service. If the principal name is <b>NULL</b>, the current user identifier is assumed. A <b>NULL</b> principal name is allowed for NTLMSSP, Kerberos, and Snego authentication services but may not work for other authentication services. For Schannel, this member must point to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the server's certificate; if it <b>NULL</b> and if a certificate for the current user does not exist, RPC_E_NO_GOOD_SECURITY_PACKAGES is returned.


### -field hr

When used in <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>, set on return to indicate the status of the call to register the authentication services.



## -see-also




<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>



<a href="https://msdn.microsoft.com/e9e7c5a3-70ec-4a68-ac21-1ab6774d140f">CoQueryAuthenticationServices</a>
 

 

