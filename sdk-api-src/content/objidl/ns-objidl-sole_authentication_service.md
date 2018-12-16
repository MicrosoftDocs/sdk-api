---
UID: NS:objidl.tagSOLE_AUTHENTICATION_SERVICE
title: SOLE_AUTHENTICATION_SERVICE
author: windows-sdk-content
description: Identifies an authentication service that a server is willing to use to communicate to a client.
old-location: com\sole_authentication_service.htm
tech.root: com
ms.assetid: 77fd15d7-54d4-4812-93d3-13a671e7afff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSOLE_AUTHENTICATION_SERVICE, PSOLE_AUTHENTICATION_SERVICE, PSOLE_AUTHENTICATION_SERVICE structure pointer [COM], SOLE_AUTHENTICATION_SERVICE, SOLE_AUTHENTICATION_SERVICE structure [COM], _com_SOLE_AUTHENTICATION_SERVICE, com.sole_authentication_service, objidlbase/PSOLE_AUTHENTICATION_SERVICE, objidlbase/SOLE_AUTHENTICATION_SERVICE, tagSOLE_AUTHENTICATION_SERVICE"
ms.topic: struct
req.header: objidl.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - SOLE_AUTHENTICATION_SERVICE
product: Windows
targetos: Windows
req.typenames: SOLE_AUTHENTICATION_SERVICE
req.redist: 
---

# SOLE_AUTHENTICATION_SERVICE structure


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
 

 

