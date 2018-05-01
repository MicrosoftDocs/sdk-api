---
UID: NF:wincred.CredMarshalCredentialA
title: CredMarshalCredentialA function
author: windows-driver-content
description: The CredMarshalCredential function transforms a credential into a text string.
old-location: security\credmarshalcredential.htm
old-project: SecAuthN
ms.assetid: 20a1d54b-04a7-4b0a-88e4-1970d1f71502
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CredMarshalCredential, CredMarshalCredential function [Security], CredMarshalCredentialA, CredMarshalCredentialW, _cred_credmarshalcredential, security.credmarshalcredential, wincred/CredMarshalCredential, wincred/CredMarshalCredentialA, wincred/CredMarshalCredentialW
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
req.unicode-ansi: CredMarshalCredentialW (Unicode) and CredMarshalCredentialA (ANSI)
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
-	CredMarshalCredential
-	CredMarshalCredentialA
-	CredMarshalCredentialW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CredMarshalCredentialA function


## -description



			The <b>CredMarshalCredential</b> function transforms a credential into a text string. Historically, many functions, such as <a href="https://msdn.microsoft.com/22550c17-003a-4f59-80f0-58fa3e286844">NetUseAdd</a>, take a domain name, user name, and password as credentials. These functions do not accept certificates as credentials. The <b>CredMarshalCredential</b> function converts such credentials into a form that can be passed into these APIs.

The marshaled credential should be passed as the user name string to any API that is currently passed credentials. The domain name, if applicable, passed to that API should be passed as <b>NULL</b> or empty. For certificate credentials, the PIN of the certificate should be passed to that API as the password.

The caller should not modify or print marshaled credentials. The returned value can be freely converted between the Unicode, ANSI, and OEM characters sets. The string is case sensitive.


## -parameters




### -param CredType [in]

Type of the credential to marshal.


### -param Credential [in]

Credential to marshal. 


This is one of the <a href="https://msdn.microsoft.com/612fdd6f-2b4c-4f41-a00b-250f90eb85d3">CRED_MARSHAL_TYPE</a> values.

If <i>CredType</i> is <i>CertCredential</i>, <i>Credential</i> points to a <a href="https://msdn.microsoft.com/acaa94c3-0562-420a-95c7-44a71374d5ea">CERT_CREDENTIAL_INFO</a> structure.

If <i>CredType</i> is <i>UsernameTargetCredential</i>, <i>Credential</i> points to a <a href="https://msdn.microsoft.com/1cb56a85-fafd-4471-b0e9-660ac0dc0219">USERNAME_TARGET_CREDENTIAL_INFO</a> structure.


### -param MarshaledCredential [out]

Pointer to a <b>null</b>-terminated 
						string that contains the marshaled credential. The caller should free the returned buffer using <a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a>.


## -returns




						This function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function can be called to get a more specific status code. The following status code can be returned:

ERROR_INVALID_PARAMETER

<i>CredType</i> is not valid.




## -see-also




<a href="https://msdn.microsoft.com/acaa94c3-0562-420a-95c7-44a71374d5ea">CERT_CREDENTIAL_INFO</a>



<a href="https://msdn.microsoft.com/612fdd6f-2b4c-4f41-a00b-250f90eb85d3">CRED_MARSHAL_TYPE</a>



<a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a>



<a href="https://msdn.microsoft.com/65757235-d92c-479f-8e2b-1f8d8564792b">CredUnmarshalCredential</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/1cb56a85-fafd-4471-b0e9-660ac0dc0219">USERNAME_TARGET_CREDENTIAL_INFO</a>
 

 

