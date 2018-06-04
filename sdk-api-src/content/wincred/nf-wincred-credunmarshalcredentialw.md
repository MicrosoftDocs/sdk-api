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

# CredUnmarshalCredentialW function


## -description



			The <b>CredUnmarshalCredential</b> function transforms a marshaled credential back into its original form.


## -parameters




### -param MarshaledCredential [in]

Pointer to a null-terminated string that contains the marshaled credential.
					


### -param CredType [out]


						Type of credential specified by <i>MarshaledCredential</i>. 


This is one of the <a href="https://msdn.microsoft.com/612fdd6f-2b4c-4f41-a00b-250f90eb85d3">CRED_MARSHAL_TYPE</a> values.


### -param Credential [out]

Pointer to the unmarshaled credential. If <i>CredType</i> returns <i>CertCredential</i>, the returned pointer is to a <a href="https://msdn.microsoft.com/acaa94c3-0562-420a-95c7-44a71374d5ea">CERT_CREDENTIAL_INFO</a> structure. If <i>CredType</i> returns <i>UsernameTargetCredential</i>, the returned pointer is to a <a href="https://msdn.microsoft.com/1cb56a85-fafd-4471-b0e9-660ac0dc0219">USERNAME_TARGET_CREDENTIAL_INFO</a> structure.

The caller should free the returned buffer using <a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a>.


## -returns




						This function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function can be called to get a more specific status code. The following status code can be returned:

ERROR_INVALID_PARAMETER

<i>MarshaledCredential</i> is not valid.




## -see-also




<a href="https://msdn.microsoft.com/acaa94c3-0562-420a-95c7-44a71374d5ea">CERT_CREDENTIAL_INFO</a>



<a href="https://msdn.microsoft.com/612fdd6f-2b4c-4f41-a00b-250f90eb85d3">CRED_MARSHAL_TYPE</a>



<a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a>



<a href="https://msdn.microsoft.com/20a1d54b-04a7-4b0a-88e4-1970d1f71502">CredMarshalCredential</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/1cb56a85-fafd-4471-b0e9-660ac0dc0219">USERNAME_TARGET_CREDENTIAL_INFO</a>
 

 

