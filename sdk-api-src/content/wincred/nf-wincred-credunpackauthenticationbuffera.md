---
UID: NF:wincred.CredUnPackAuthenticationBufferA
title: CredUnPackAuthenticationBufferA function (wincred.h)
description: Converts an authentication buffer returned by a call to the CredUIPromptForWindowsCredentials function into a string user name and password. (ANSI)
helpviewer_keywords: ["CredUnPackAuthenticationBufferA", "wincred/CredUnPackAuthenticationBufferA"]
old-location: security\credunpackauthenticationbuffer.htm
tech.root: security
ms.assetid: c87f0b11-59c2-4450-ad63-398cdb15016f
ms.date: 12/05/2018
ms.keywords: CredUnPackAuthenticationBuffer, CredUnPackAuthenticationBuffer function [Security], CredUnPackAuthenticationBufferA, CredUnPackAuthenticationBufferW, security.credunpackauthenticationbuffer, wincred/CredUnPackAuthenticationBuffer, wincred/CredUnPackAuthenticationBufferA, wincred/CredUnPackAuthenticationBufferW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredUnPackAuthenticationBufferW (Unicode) and CredUnPackAuthenticationBufferA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredUnPackAuthenticationBufferA
 - wincred/CredUnPackAuthenticationBufferA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-0.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - CredUnPackAuthenticationBuffer
 - CredUnPackAuthenticationBufferA
 - CredUnPackAuthenticationBufferW
---

# CredUnPackAuthenticationBufferA function


## -description

The <b>CredUnPackAuthenticationBuffer</b> function converts an authentication buffer returned by a call to the <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> function into a string user name and password.

## -parameters

### -param dwFlags [in]

Setting the value of this parameter to <b>CRED_PACK_PROTECTED_CREDENTIALS</b> specifies that the function attempts to decrypt the credentials in the authentication buffer. If the credential  cannot be decrypted, the function returns <b>FALSE</b>, and a call to the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function will return the value <b>ERROR_NOT_CAPABLE</b>.

How the decryption is done depends on the format of the authentication buffer.

If the authentication buffer is a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure, the function can decrypt the buffer if it is encrypted by using <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a> with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option.

If the authentication buffer is one of the marshaled KERB_*_LOGON structures, the function decrypts the password before returning it in the <i>pszPassword</i> buffer.

### -param pAuthBuffer [in]

A pointer to the authentication buffer to be converted.

This buffer is typically the output of the <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> or <a href="/windows/desktop/api/wincred/nf-wincred-credpackauthenticationbuffera">CredPackAuthenticationBuffer</a> function. This must be one of the following types:<ul>
<li>A <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure for identity credentials. The function does not accept other <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structures.</li>
<li>A <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon">KERB_INTERACTIVE_LOGON</a> or <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_unlock_logon">KERB_INTERACTIVE_UNLOCK_LOGON</a>  structure for password credentials.</li>
<li>A <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon">KERB_CERTIFICATE_LOGON</a> or <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_unlock_logon">KERB_CERTIFICATE_UNLOCK_LOGON</a>  structure for smart card certificate credentials.</li>
<li>GENERIC_CRED for generic credentials.</li>
</ul>

### -param cbAuthBuffer [in]

The size, in bytes, of the <i>pAuthBuffer</i> buffer.

### -param pszUserName [out]

A pointer to a null-terminated string that receives the user name.

This string can be a marshaled credential. See Remarks.

### -param pcchlMaxUserName [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in characters, of the <i>pszUserName</i> buffer. On output, if the buffer is not of sufficient size, specifies the required size, in characters, of the  <i>pszUserName</i> buffer. The size includes terminating null character.

### -param pszDomainName [out]

A pointer to a null-terminated string that receives the name of the user's domain.

### -param pcchMaxDomainName [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in characters, of the <i>pszDomainName</i> buffer. On output, if the buffer is not of sufficient size, specifies the required size, in characters, of the  <i>pszDomainName</i> buffer. The size includes the terminating null character. The required size can be zero if there is no domain name.

### -param pszPassword [out]

A pointer to a null-terminated string that receives the password.

### -param pcchMaxPassword [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in characters, of the <i>pszPassword</i> buffer. On output, if the buffer is not of sufficient size, specifies the required size, in characters, of the  <i>pszPassword</i> buffer. The size includes the terminating null character.  

This string can be a marshaled credential. See Remarks.

## -returns

<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.

For extended error information, call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. The following table shows common values for the <b>GetLastError</b> function.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CAPABLE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
CRED_PACK_PROTECTED_CREDENTIALS was passed as the value of the <i>dwFlags</i> parameter, but this function cannot decrypt the credential because the security context used to protect the password is different from the security context of the caller.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
One of the output buffers, <i>pszUserName</i>, <i>pszDomainName</i>, or <i>pszPassword</i>,  was of insufficient size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The authentication buffer is not of a supported type.

</td>
</tr>
</table>

## -remarks

Beginning with  Windows 8 and Windows Server 2012, the authentication buffer can be a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure, which can be optionally encrypted by using the <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option. This credential format is returned by a Credential Provider of an Identity Provider by using the <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> or <a href="/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa">SspiPromptForCredentials</a> function. This structure can also be constructed by using the <a href="/windows/desktop/api/wincred/nf-wincred-credpackauthenticationbuffera">CredPackAuthenticationBuffer</a> function. 
If the authentication buffer <i>pAuthBuffer</i> represents a nonpassword credential, such as <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon">KERB_CERTIFICATE_LOGON</a> or <b>SEC_WINNT_AUTH_IDENTITY_EX2</b>, the function must marshal the credential as character strings, returned as user name, domain name, and password strings. The marshaling is done by using a specific procedure. When <i>dwFlags</i> contains the CRED_PACK_PROTECTED_CREDENTIALS flag, the caller must run in the same logon session in which the credential was encrypted.





> [!NOTE]
> The wincred.h header defines CredUnPackAuthenticationBuffer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
