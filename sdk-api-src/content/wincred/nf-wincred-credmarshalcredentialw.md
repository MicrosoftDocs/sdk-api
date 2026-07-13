---
UID: NF:wincred.CredMarshalCredentialW
title: CredMarshalCredentialW function (wincred.h)
description: The CredMarshalCredential function transforms a credential into a text string. (Unicode)
helpviewer_keywords: ["CredMarshalCredential", "CredMarshalCredential function [Security]", "CredMarshalCredentialW", "_cred_credmarshalcredential", "security.credmarshalcredential", "wincred/CredMarshalCredential", "wincred/CredMarshalCredentialW"]
old-location: security\credmarshalcredential.htm
tech.root: security
ms.assetid: 20a1d54b-04a7-4b0a-88e4-1970d1f71502
ms.date: 12/05/2018
ms.keywords: CredMarshalCredential, CredMarshalCredential function [Security], CredMarshalCredentialA, CredMarshalCredentialW, _cred_credmarshalcredential, security.credmarshalcredential, wincred/CredMarshalCredential, wincred/CredMarshalCredentialA, wincred/CredMarshalCredentialW
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredMarshalCredentialW
 - wincred/CredMarshalCredentialW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredMarshalCredential
 - CredMarshalCredentialA
 - CredMarshalCredentialW
---

# CredMarshalCredentialW function


## -description

The <b>CredMarshalCredential</b> function transforms a credential into a text string. Historically, many functions, such as <a href="/windows/desktop/api/lmuse/nf-lmuse-netuseadd">NetUseAdd</a>, take a domain name, user name, and password as credentials. These functions do not accept certificates as credentials. The <b>CredMarshalCredential</b> function converts such credentials into a form that can be passed into these APIs.

The marshaled credential should be passed as the user name string to any API that is currently passed credentials. The domain name, if applicable, passed to that API should be passed as <b>NULL</b> or empty. For certificate credentials, the PIN of the certificate should be passed to that API as the password.

The caller should not modify or print marshaled credentials. The returned value can be freely converted between the Unicode, ANSI, and OEM characters sets. The string is case sensitive.

## -parameters

### -param CredType [in]

Type of the credential to marshal.

### -param Credential [in]

Credential to marshal. 


This is one of the <a href="/windows/desktop/api/wincred/ne-wincred-cred_marshal_type">CRED_MARSHAL_TYPE</a> values.

If <i>CredType</i> is <i>CertCredential</i>, <i>Credential</i> points to a <a href="/windows/desktop/api/wincred/ns-wincred-cert_credential_info">CERT_CREDENTIAL_INFO</a> structure.

If <i>CredType</i> is <i>UsernameTargetCredential</i>, <i>Credential</i> points to a <a href="/windows/desktop/api/wincred/ns-wincred-username_target_credential_info">USERNAME_TARGET_CREDENTIAL_INFO</a> structure.

### -param MarshaledCredential [out]

Pointer to a <b>null</b>-terminated 
						string that contains the marshaled credential. The caller should free the returned buffer using <a href="/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>.

## -returns

This function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function can be called to get a more specific status code. The following status code can be returned:

ERROR_INVALID_PARAMETER

<i>CredType</i> is not valid.

## -see-also

<a href="/windows/desktop/api/wincred/ns-wincred-cert_credential_info">CERT_CREDENTIAL_INFO</a>



<a href="/windows/desktop/api/wincred/ne-wincred-cred_marshal_type">CRED_MARSHAL_TYPE</a>



<a href="/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>



<a href="/windows/desktop/api/wincred/nf-wincred-credunmarshalcredentiala">CredUnmarshalCredential</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/wincred/ns-wincred-username_target_credential_info">USERNAME_TARGET_CREDENTIAL_INFO</a>

## -remarks

> [!NOTE]
> The wincred.h header defines CredMarshalCredential as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
