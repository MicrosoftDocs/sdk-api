---
UID: NF:wincred.CredUnmarshalCredentialW
title: CredUnmarshalCredentialW function
author: windows-driver-content
description: The CredUnmarshalCredential function transforms a marshaled credential back into its original form.
old-location: security\credunmarshalcredential.htm
old-project: SecAuthN
ms.assetid: 65757235-d92c-479f-8e2b-1f8d8564792b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: CredUnmarshalCredential, CredUnmarshalCredential function [Security], CredUnmarshalCredentialA, CredUnmarshalCredentialW, _cred_credunmarshalcredential, security.credunmarshalcredential, wincred/CredUnmarshalCredential, wincred/CredUnmarshalCredentialA, wincred/CredUnmarshalCredentialW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredUnmarshalCredentialW (Unicode) and CredUnmarshalCredentialA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRED_PROTECTION_TYPE, *PCRED_PROTECTION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
-	sechost.dll
-	API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
-	CredUnmarshalCredential
-	CredUnmarshalCredentialA
-	CredUnmarshalCredentialW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

