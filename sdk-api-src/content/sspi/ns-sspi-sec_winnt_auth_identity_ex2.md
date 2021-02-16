---
UID: NS:sspi._SEC_WINNT_AUTH_IDENTITY_EX2
title: SEC_WINNT_AUTH_IDENTITY_EX2 (sspi.h)
description: Contains information about an authentication identity.
helpviewer_keywords: ["*PSEC_WINNT_AUTH_IDENTITY_EX2","PSEC_WINNT_AUTH_IDENTITY_EX2","PSEC_WINNT_AUTH_IDENTITY_EX2 structure pointer [Security]","SEC_WINNT_AUTH_IDENTITY_ANSI","SEC_WINNT_AUTH_IDENTITY_EX2","SEC_WINNT_AUTH_IDENTITY_EX2 structure [Security]","SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER","SEC_WINNT_AUTH_IDENTITY_FLAGS_PROCESS_ENCRYPTED","SEC_WINNT_AUTH_IDENTITY_FLAGS_RESERVED","SEC_WINNT_AUTH_IDENTITY_FLAGS_SYSTEM_PROTECTED","SEC_WINNT_AUTH_IDENTITY_FLAGS_USER_PROTECTED","SEC_WINNT_AUTH_IDENTITY_MARSHALLED","SEC_WINNT_AUTH_IDENTITY_ONLY","SEC_WINNT_AUTH_IDENTITY_UNICODE","security.sec_winnt_auth_identity_ex2","sspi/PSEC_WINNT_AUTH_IDENTITY_EX2","sspi/SEC_WINNT_AUTH_IDENTITY_EX2"]
old-location: security\sec_winnt_auth_identity_ex2.htm
tech.root: security
ms.assetid: a6083d76-1774-428c-85ca-fea817827d6a
ms.date: 12/05/2018
ms.keywords: '*PSEC_WINNT_AUTH_IDENTITY_EX2, PSEC_WINNT_AUTH_IDENTITY_EX2, PSEC_WINNT_AUTH_IDENTITY_EX2 structure pointer [Security], SEC_WINNT_AUTH_IDENTITY_ANSI, SEC_WINNT_AUTH_IDENTITY_EX2, SEC_WINNT_AUTH_IDENTITY_EX2 structure [Security], SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER, SEC_WINNT_AUTH_IDENTITY_FLAGS_PROCESS_ENCRYPTED, SEC_WINNT_AUTH_IDENTITY_FLAGS_RESERVED, SEC_WINNT_AUTH_IDENTITY_FLAGS_SYSTEM_PROTECTED, SEC_WINNT_AUTH_IDENTITY_FLAGS_USER_PROTECTED, SEC_WINNT_AUTH_IDENTITY_MARSHALLED, SEC_WINNT_AUTH_IDENTITY_ONLY, SEC_WINNT_AUTH_IDENTITY_UNICODE, security.sec_winnt_auth_identity_ex2, sspi/PSEC_WINNT_AUTH_IDENTITY_EX2, sspi/SEC_WINNT_AUTH_IDENTITY_EX2'
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: SEC_WINNT_AUTH_IDENTITY_EX2, *PSEC_WINNT_AUTH_IDENTITY_EX2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_WINNT_AUTH_IDENTITY_EX2
 - sspi/_SEC_WINNT_AUTH_IDENTITY_EX2
 - PSEC_WINNT_AUTH_IDENTITY_EX2
 - sspi/PSEC_WINNT_AUTH_IDENTITY_EX2
 - SEC_WINNT_AUTH_IDENTITY_EX2
 - sspi/SEC_WINNT_AUTH_IDENTITY_EX2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SEC_WINNT_AUTH_IDENTITY_EX2
---

# SEC_WINNT_AUTH_IDENTITY_EX2 structure


## -description

Contains information about an authentication identity. The <b>SEC_WINNT_AUTH_IDENTITY_EX2</b> structure contains authentication data that is provided to the <a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a> function.

## -struct-fields

### -field Version

The version number of the structure. This must be <b>SEC_WINNT_AUTH_IDENTITY_VERSION_2</b>.

### -field cbHeaderLength

The size, in bytes, of the structure header.

### -field cbStructureLength

The size, in bytes, of the structure.

### -field UserOffset

The offset from the beginning of the structure to the beginning of the user name string.

### -field UserLength

The size, in bytes, of the user name string.

### -field DomainOffset

The offset from the beginning of the structure to the beginning of the domain name string. 

An identity credential should contain the identity provider name instead of the domain name.

### -field DomainLength

The size, in bytes, of the domain name string.

### -field PackedCredentialsOffset

The offset from the beginning of the structure to the beginning of the packed credentials.

The packed credential is a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_packed_credentials">SEC_WINNT_AUTH_PACKED_CREDENTIALS</a> structure that contains a credential type that uniquely specifies the credential type.

### -field PackedCredentialsLength

The size, in bytes, of the packed credentials string.

### -field Flags

An <b>unsigned long</b> flag that indicates the type used by negotiable <a href="/windows/desktop/SecGloss/s-gly">security packages</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_MARSHALLED"></a><a id="sec_winnt_auth_identity_marshalled"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_MARSHALLED</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
All data is in one buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_ONLY"></a><a id="sec_winnt_auth_identity_only"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_ONLY</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
Used with the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP). Credentials are for identity only. The Kerberos package is directed to not include authorization data in the ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_ANSI"></a><a id="sec_winnt_auth_identity_ansi"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_ANSI</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Credentials are in ANSI form.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_UNICODE"></a><a id="sec_winnt_auth_identity_unicode"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_UNICODE</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
Credentials are in Unicode form.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER"></a><a id="sec_winnt_auth_identity_flags_id_provider"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER</b></dt>
<dt>524288 (0x80000)</dt>
</dl>
</td>
<td width="60%">
When the credential type is password, the presence of this flag specifies that the structure is an online ID credential.  The <b>DomainOffset</b> and <b>DomainLength</b> members correspond to the online ID provider name.

<b>Windows Server 2008 R2 and Windows 7:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_FLAGS_PROCESS_ENCRYPTED"></a><a id="sec_winnt_auth_identity_flags_process_encrypted"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_FLAGS_PROCESS_ENCRYPTED</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
The structure is encrypted by the <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentity">SspiEncryptAuthIdentity</a> function or by  the <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_PROCESS option. It can only be decrypted by the same process.

<b>Windows Server 2008 R2 and Windows 7:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_FLAGS_SYSTEM_PROTECTED"></a><a id="sec_winnt_auth_identity_flags_system_protected"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_FLAGS_SYSTEM_PROTECTED</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
The structure is encrypted by the <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option under the SYSTEM security context. It can only be decrypted by a thread running as SYSTEM.

<b>Windows Server 2008 R2 and Windows 7:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_FLAGS_USER_PROTECTED"></a><a id="sec_winnt_auth_identity_flags_user_protected"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_FLAGS_USER_PROTECTED</b></dt>
<dt>64 (0x40)</dt>
</dl>
</td>
<td width="60%">
The structure is encrypted by the <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option under a non-SYSTEM security context. It can only be decrypted by a thread running in the same logon session in which it was encrypted.

<b>Windows Server 2008 R2 and Windows 7:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_FLAGS_RESERVED"></a><a id="sec_winnt_auth_identity_flags_reserved"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_FLAGS_RESERVED</b></dt>
<dt>65536 (0x10000)</dt>
</dl>
</td>
<td width="60%">
The authentication identity buffer is <b>cbStructureLength</b> + 8 padding bytes that are necessary for in-place encryption or decryption of the identity.

</td>
</tr>
</table>

### -field PackageListOffset

The offset from the beginning of the structure to the beginning of the list of supported packages.

### -field PackageListLength

The size, in bytes, of the supported package list.

## -remarks

This authentication identity buffer can be returned from several credential APIs, for example, the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getserialization">GetSerialization</a> method and the <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredential</a> and <a href="/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa">SspiPromptForCredentials</a> functions.

The structure describes a header of the authentication identity buffer and the data is appended at the end of the structure. Although the buffer size is specified by the <b>cbStructureLength</b> member, the actual buffer size can be larger or smaller than <b>cbStructureLength</b>. Some functions, such as <a href="/windows/desktop/api/sspi/nf-sspi-sspivalidateauthidentity">SspiValidateAuthIdentity</a>, take a pointer, but not the buffer size, to the identity structure as input. As a result, those functions can validate the internal buffer data but cannot verify the buffer size. This can result in reading or writing data outside of the buffer range. To avoid buffer overruns when handling an untrusted identity buffer, applications should call <a href="/windows/desktop/api/sspi/nf-sspi-sspiunmarshalauthidentity">SspiUnmarshalAuthIdentity</a> to obtain a pointer to an identity structure with a validated size and then pass that pointer to the functions.

The <b>SEC_WINNT_AUTH_IDENTITY_EX2</b> structure can be returned by <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes(CredSSP)</a> and consumed by <a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle(CredSSP)</a>, <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>, and other identity provider interfaces.


<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_packed_credentials">SEC_WINNT_AUTH_PACKED_CREDENTIALS</a> can contain a password credential type, defined as SEC_WINNT_AUTH_DATA_TYPE_PASSWORD. This credential type describes password credentials of a domain user as well as other online identities. Applications must define _SEC_WINNT_AUTH_TYPES to compile code that references this credential type as well as other definitions of the <b>SEC_WINNT_AUTH_PACKED_CREDENTIALS</b> structure.

Applications should not query or set the <b>Flags</b> member directly. Use the   <a href="/windows/desktop/api/sspi/nf-sspi-sspiisauthidentityencrypted">SspiIsAuthIdentityEncrypted</a>,  <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a>, and  <a href="/windows/desktop/api/sspi/nf-sspi-sspidecryptauthidentityex">SspiDecryptAuthIdentityEx</a> functions to manage the encryption and decryption of the <b>SEC_WINNT_AUTH_IDENTITY_EX2</b> structure.

Identity providers must explicitly check or set SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER and the domain name fields to differentiate their password credential from a domain password and another identity provider's password.

The <a href="/windows/desktop/api/wincred/nf-wincred-credpackauthenticationbuffera">CredPackAuthenticationBuffer</a> function  can be called with the CRED_PACK_ID_PROVIDER_CREDENTIALS option to create a <b>SEC_WINNT_AUTH_IDENTITY_EX2</b> structure with the authentication data of SEC_WINNT_AUTH_DATA_TYPE_PASSWORD credential type, a <b>Flags</b> member that contains the SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER value, and a <b>DomainOffset</b> member set to the provider name.