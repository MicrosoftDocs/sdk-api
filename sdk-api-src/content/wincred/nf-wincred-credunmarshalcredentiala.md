---
UID: NF:wincred.CredUnmarshalCredentialA
title: CredUnmarshalCredentialA function (wincred.h)
author: windows-sdk-content
description: The CredUnmarshalCredential function transforms a marshaled credential back into its original form.
old-location: security\credunmarshalcredential.htm
tech.root: SecAuthN
ms.assetid: 65757235-d92c-479f-8e2b-1f8d8564792b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CredUnmarshalCredential, CredUnmarshalCredential function [Security], CredUnmarshalCredentialA, CredUnmarshalCredentialW, _cred_credunmarshalcredential, security.credunmarshalcredential, wincred/CredUnmarshalCredential, wincred/CredUnmarshalCredentialA, wincred/CredUnmarshalCredentialW
ms.topic: function
f1_keywords:
- wincred/CredUnmarshalCredential
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
- sechost.dll
- API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
- CredUnmarshalCredential
- CredUnmarshalCredentialA
- CredUnmarshalCredentialW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CredUnmarshalCredentialA function


## -description


The <b>CredUnmarshalCredential</b> function transforms a marshaled credential back into its original form.


## -parameters




### -param MarshaledCredential [in]

Pointer to a null-terminated string that contains the marshaled credential.
					


### -param CredType [out]

Type of credential specified by <i>MarshaledCredential</i>. 


This is one of the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/ne-wincred-cred_marshal_type">CRED_MARSHAL_TYPE</a> values.


### -param Credential [out]

Pointer to the unmarshaled credential. If <i>CredType</i> returns <i>CertCredential</i>, the returned pointer is to a <a href="https://docs.microsoft.com/windows/desktop/api/wincred/ns-wincred-cert_credential_info">CERT_CREDENTIAL_INFO</a> structure. If <i>CredType</i> returns <i>UsernameTargetCredential</i>, the returned pointer is to a <a href="https://docs.microsoft.com/windows/desktop/api/wincred/ns-wincred-username_target_credential_info">USERNAME_TARGET_CREDENTIAL_INFO</a> structure.

The caller should free the returned buffer using <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>.


## -returns



This function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function can be called to get a more specific status code. The following status code can be returned:

ERROR_INVALID_PARAMETER

<i>MarshaledCredential</i> is not valid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincred/ns-wincred-cert_credential_info">CERT_CREDENTIAL_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincred/ne-wincred-cred_marshal_type">CRED_MARSHAL_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincred/ns-wincred-username_target_credential_info">USERNAME_TARGET_CREDENTIAL_INFO</a>
 

 

