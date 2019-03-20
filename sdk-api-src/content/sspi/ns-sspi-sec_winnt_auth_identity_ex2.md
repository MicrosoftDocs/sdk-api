---
UID: NS:sspi._SEC_WINNT_AUTH_IDENTITY_EX2
title: SEC_WINNT_AUTH_IDENTITY_EX2 (sspi.h)
author: windows-sdk-content
description: Contains information about an authentication identity.
old-location: security\sec_winnt_auth_identity_ex2.htm
tech.root: SecAuthN
ms.assetid: a6083d76-1774-428c-85ca-fea817827d6a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSEC_WINNT_AUTH_IDENTITY_EX2, PSEC_WINNT_AUTH_IDENTITY_EX2, PSEC_WINNT_AUTH_IDENTITY_EX2 structure pointer [Security], SEC_WINNT_AUTH_IDENTITY_ANSI, SEC_WINNT_AUTH_IDENTITY_EX2, SEC_WINNT_AUTH_IDENTITY_EX2 structure [Security], SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER, SEC_WINNT_AUTH_IDENTITY_FLAGS_PROCESS_ENCRYPTED, SEC_WINNT_AUTH_IDENTITY_FLAGS_RESERVED, SEC_WINNT_AUTH_IDENTITY_FLAGS_SYSTEM_PROTECTED, SEC_WINNT_AUTH_IDENTITY_FLAGS_USER_PROTECTED, SEC_WINNT_AUTH_IDENTITY_MARSHALLED, SEC_WINNT_AUTH_IDENTITY_ONLY, SEC_WINNT_AUTH_IDENTITY_UNICODE, security.sec_winnt_auth_identity_ex2, sspi/PSEC_WINNT_AUTH_IDENTITY_EX2, sspi/SEC_WINNT_AUTH_IDENTITY_EX2"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SEC_WINNT_AUTH_IDENTITY_EX2
product: Windows
targetos: Windows
req.typenames: SEC_WINNT_AUTH_IDENTITY_EX2, *PSEC_WINNT_AUTH_IDENTITY_EX2
req.redist: 
---

# SEC_WINNT_AUTH_IDENTITY_EX2 structure


## -description


Contains information about an authentication identity. The <b>SEC_WINNT_AUTH_IDENTITY_EX2</b> structure contains authentication data that is provided to the <a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle</a> function.


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

The packed credential is a <a href="https://msdn.microsoft.com/9a21f0cd-d4e1-4aa8-8d0d-72bc7002ce32">SEC_WINNT_AUTH_PACKED_CREDENTIALS</a> structure that contains a credential type that uniquely specifies the credential type.


### -field PackedCredentialsLength

The size, in bytes, of the packed credentials string.


### -field Flags

An <b>unsigned long</b> flag that indicates the type used by negotiable <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security packages</a>.

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
Used with the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP). Credentials are for identity only. The Kerberos package is directed to not include authorization data in the ticket.

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
The structure is encrypted by the <a href="https://msdn.microsoft.com/4460f7ec-35fd-4ad1-8c20-dda9f4d3477a">SspiEncryptAuthIdentity</a> function or by  the <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_PROCESS option. It can only be decrypted by the same process.

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
The structure is encrypted by the <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option under the SYSTEM security context. It can only be decrypted by a thread running as SYSTEM.

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
The structure is encrypted by the <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option under a non-SYSTEM security context. It can only be decrypted by a thread running in the same logon session in which it was encrypted.

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



This authentication identity buffer can be returned from several credential APIs, for example, the <a href="https://msdn.microsoft.com/c5f7ba25-c38a-431a-b4ad-0e2409f763a3">GetSerialization</a> method and the <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredential</a> and <a href="https://msdn.microsoft.com/2af2ac00-0e91-4384-9ffa-3e100df218c1">SspiPromptForCredentials</a> functions.

The structure describes a header of the authentication identity buffer and the data is appended at the end of the structure. Although the buffer size is specified by the <b>cbStructureLength</b> member, the actual buffer size can be larger or smaller than <b>cbStructureLength</b>. Some functions, such as <a href="https://msdn.microsoft.com/82733abd-d984-4902-b6e4-c3809171ad51">SspiValidateAuthIdentity</a>, take a pointer, but not the buffer size, to the identity structure as input. As a result, those functions can validate the internal buffer data but cannot verify the buffer size. This can result in reading or writing data outside of the buffer range. To avoid buffer overruns when handling an untrusted identity buffer, applications should call <a href="https://msdn.microsoft.com/89798b37-808a-4174-8362-a2dc4ee1b460">SspiUnmarshalAuthIdentity</a> to obtain a pointer to an identity structure with a validated size and then pass that pointer to the functions.

The <b>SEC_WINNT_AUTH_IDENTITY_EX2</b> structure can be returned by <a href="https://msdn.microsoft.com/4956c4ab-b71e-4960-b750-f3a79b87baac">QueryContextAttributes(CredSSP)</a> and consumed by <a href="https://msdn.microsoft.com/3b73decf-75d4-4bc4-b7ca-5f16aaadff29">AcquireCredentialsHandle(CredSSP)</a>, <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>, and other identity provider interfaces.


<a href="https://msdn.microsoft.com/9a21f0cd-d4e1-4aa8-8d0d-72bc7002ce32">SEC_WINNT_AUTH_PACKED_CREDENTIALS</a> can contain a password credential type, defined as SEC_WINNT_AUTH_DATA_TYPE_PASSWORD. This credential type describes password credentials of a domain user as well as other online identities. Applications must define _SEC_WINNT_AUTH_TYPES to compile code that references this credential type as well as other definitions of the <b>SEC_WINNT_AUTH_PACKED_CREDENTIALS</b> structure.

Applications should not query or set the <b>Flags</b> member directly. Use the   <a href="https://msdn.microsoft.com/b85095f5-0ca5-4d75-866d-9b756404c1d9">SspiIsAuthIdentityEncrypted</a>,  <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a>, and  <a href="https://msdn.microsoft.com/86598BAA-0E87-46A9-AA1A-BF04BF0CDAFA">SspiDecryptAuthIdentityEx</a> functions to manage the encryption and decryption of the <b>SEC_WINNT_AUTH_IDENTITY_EX2</b> structure.

Identity providers must explicitly check or set SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER and the domain name fields to differentiate their password credential from a domain password and another identity provider's password.

The <a href="https://msdn.microsoft.com/48ffdd7a-1969-4f6a-bbc7-2826e21ea052">CredPackAuthenticationBuffer</a> function  can be called with the CRED_PACK_ID_PROVIDER_CREDENTIALS option to create a <b>SEC_WINNT_AUTH_IDENTITY_EX2</b> structure with the authentication data of SEC_WINNT_AUTH_DATA_TYPE_PASSWORD credential type, a <b>Flags</b> member that contains the SEC_WINNT_AUTH_IDENTITY_FLAGS_ID_PROVIDER value, and a <b>DomainOffset</b> member set to the provider name.



