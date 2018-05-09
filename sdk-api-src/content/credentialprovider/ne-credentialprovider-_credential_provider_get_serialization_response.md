---
UID: NE:credentialprovider._CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE
title: "_CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE"
author: windows-driver-content
description: Describes the response when a credential provider attempts to serialize credentials.
old-location: shell\CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE.htm
old-project: shell
ms.assetid: 73615129-62f2-4bc9-acf6-058a6641f4e2
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: CPGSR_NO_CREDENTIAL_FINISHED, CPGSR_NO_CREDENTIAL_NOT_FINISHED, CPGSR_RETURN_CREDENTIAL_FINISHED, CPGSR_RETURN_NO_CREDENTIAL_FINISHED, CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE, CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE enumeration [Windows Shell], _CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE, _shell_CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE, credentialprovider/CPGSR_NO_CREDENTIAL_FINISHED, credentialprovider/CPGSR_NO_CREDENTIAL_NOT_FINISHED, credentialprovider/CPGSR_RETURN_CREDENTIAL_FINISHED, credentialprovider/CPGSR_RETURN_NO_CREDENTIAL_FINISHED, credentialprovider/CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE, shell.CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Credentialprovider.h
api_name:
-	CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE enumeration


## -description


Describes the response when a credential provider attempts to serialize credentials. Used by <a href="https://msdn.microsoft.com/c5f7ba25-c38a-431a-b4ad-0e2409f763a3">ICredentialProviderCredential::GetSerialization</a>.


## -enum-fields




### -field CPGSR_NO_CREDENTIAL_NOT_FINISHED

No credential was serialized because more information is needed. One example of this would be if a credential requires both a PIN and an answer to a secret question, but the user has only provided the PIN. This signals the caller should be given a chance to alter its response.


### -field CPGSR_NO_CREDENTIAL_FINISHED

The credential provider has not serialized a credential but has completed its work. This response has multiple meanings. It can mean that no credential was serialized and that the user should not try again. This response can also mean that no credential was submitted but the credential's work is complete. For example, in the Change Password scenario, this response implies success.


### -field CPGSR_RETURN_CREDENTIAL_FINISHED

A credential was serialized. This response implies that a serialization structure was passed back.


### -field CPGSR_RETURN_NO_CREDENTIAL_FINISHED

The credential provider has not serialized a credential, but has completed its work. The difference between this value and <b>CPGSR_NO_CREDENTIAL_FINISHED</b> is that this flag will force the logon UI to return, which will call <a href="https://msdn.microsoft.com/d971c7be-f440-41ce-945d-4dbe51554e59">UnAdvise</a> for all the credential providers.


## -see-also




<a href="https://msdn.microsoft.com/BCF69196-D4E4-41D0-B372-5000FD50164B">Credential Providers in Windows 10</a>
 

 

