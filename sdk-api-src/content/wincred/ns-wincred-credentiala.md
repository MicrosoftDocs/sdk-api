---
UID: NS:wincred._CREDENTIALA
title: CREDENTIALA (wincred.h)
description: The CREDENTIAL structure contains an individual credential.
helpviewer_keywords: ["*PCREDENTIALA","CREDENTIAL","CREDENTIAL structure [Security]","CREDENTIALA","CREDENTIALW","CRED_FLAGS_PROMPT_NOW","CRED_FLAGS_USERNAME_TARGET","CRED_PERSIST_ENTERPRISE","CRED_PERSIST_LOCAL_MACHINE","CRED_PERSIST_SESSION","CRED_TYPE_DOMAIN_CERTIFICATE","CRED_TYPE_DOMAIN_EXTENDED","CRED_TYPE_DOMAIN_PASSWORD","CRED_TYPE_DOMAIN_VISIBLE_PASSWORD","CRED_TYPE_GENERIC","CRED_TYPE_GENERIC_CERTIFICATE","CRED_TYPE_MAXIMUM","CRED_TYPE_MAXIMUM_EX","PCREDENTIAL","PCREDENTIAL structure pointer [Security]","_cred_credential","security.credential","wincred/CREDENTIAL","wincred/CREDENTIALA","wincred/CREDENTIALW","wincred/PCREDENTIAL"]
old-location: security\credential.htm
tech.root: security
ms.assetid: 6361b93c-4441-4a01-bd39-b95c42962497
ms.date: 12/05/2018
ms.keywords: '*PCREDENTIALA, CREDENTIAL, CREDENTIAL structure [Security], CREDENTIALA, CREDENTIALW, CRED_FLAGS_PROMPT_NOW, CRED_FLAGS_USERNAME_TARGET, CRED_PERSIST_ENTERPRISE, CRED_PERSIST_LOCAL_MACHINE, CRED_PERSIST_SESSION, CRED_TYPE_DOMAIN_CERTIFICATE, CRED_TYPE_DOMAIN_EXTENDED, CRED_TYPE_DOMAIN_PASSWORD, CRED_TYPE_DOMAIN_VISIBLE_PASSWORD, CRED_TYPE_GENERIC, CRED_TYPE_GENERIC_CERTIFICATE, CRED_TYPE_MAXIMUM, CRED_TYPE_MAXIMUM_EX, PCREDENTIAL, PCREDENTIAL structure pointer [Security], _cred_credential, security.credential, wincred/CREDENTIAL, wincred/CREDENTIALA, wincred/CREDENTIALW, wincred/PCREDENTIAL'
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CREDENTIALW (Unicode) and CREDENTIALA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREDENTIALA, *PCREDENTIALA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDENTIALA
 - wincred/_CREDENTIALA
 - PCREDENTIALA
 - wincred/PCREDENTIALA
 - CREDENTIALA
 - wincred/CREDENTIALA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CREDENTIAL
 - CREDENTIALA
 - CREDENTIALW
---

# CREDENTIALA structure


## -description

The <b>CREDENTIAL</b> structure contains an individual credential.

## -struct-fields

### -field Flags

A bit member that identifies characteristics of the credential. Undefined bits should be initialized as zero and not otherwise altered to permit future enhancement.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRED_FLAGS_PROMPT_NOW"></a><a id="cred_flags_prompt_now"></a><dl>
<dt><b><b>CRED_FLAGS_PROMPT_NOW</b></b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
Bit set if the credential does not persist the <b>CredentialBlob</b> and the credential has not been written during this logon session. This bit is ignored on input and is set automatically when queried.

If <b>Type</b> is <b>CRED_TYPE_DOMAIN_CERTIFICATE</b>, the <b>CredentialBlob</b> is not persisted across logon sessions because the PIN of a certificate is very sensitive information. Indeed, when the credential is written to credential manager, the PIN is passed to the CSP associated with the certificate. The CSP will enforce a PIN retention policy appropriate to the certificate.

If <b>Type</b> is <b>CRED_TYPE_DOMAIN_PASSWORD</b> or <b>CRED_TYPE_DOMAIN_CERTIFICATE</b>, an authentication package always fails an authentication attempt when using credentials marked as <b>CRED_FLAGS_PROMPT_NOW</b>. The application (typically through the key ring UI) prompts the user for the password. The application saves the credential and retries the authentication. Because the credential has been recently written, the authentication package now gets a credential that is not marked as CRED_FLAGS_PROMPT_NOW.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_FLAGS_USERNAME_TARGET"></a><a id="cred_flags_username_target"></a><dl>
<dt><b><b>CRED_FLAGS_USERNAME_TARGET</b></b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
Bit is set if this credential has a <b>TargetName</b> member set to the same value as the <b>UserName</b> member. Such a credential is one designed to store the <b>CredentialBlob</b> for a specific user. For more information, see the <a href="/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a> function.

This bit can only be specified if <b>Type</b> is <b>CRED_TYPE_DOMAIN_PASSWORD</b> or <b>CRED_TYPE_DOMAIN_CERTIFICATE</b>.

</td>
</tr>
</table>

### -field Type

The type of the credential. This member cannot be changed after the credential is created. The following values are valid.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRED_TYPE_GENERIC"></a><a id="cred_type_generic"></a><dl>
<dt><b><b>CRED_TYPE_GENERIC</b></b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The credential is a generic credential. The credential will not be used by any particular authentication package. The credential will be stored securely but has no other significant characteristics.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_TYPE_DOMAIN_PASSWORD"></a><a id="cred_type_domain_password"></a><dl>
<dt><b><b>CRED_TYPE_DOMAIN_PASSWORD</b></b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The credential is a password credential and is specific to Microsoft's authentication packages. The NTLM, Kerberos, and Negotiate authentication packages will automatically use this credential when connecting to the named target.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_TYPE_DOMAIN_CERTIFICATE"></a><a id="cred_type_domain_certificate"></a><dl>
<dt><b><b>CRED_TYPE_DOMAIN_CERTIFICATE</b></b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
The credential is a certificate credential and is specific to Microsoft's authentication packages. The Kerberos, Negotiate, and Schannel authentication packages automatically use this credential when connecting to the named target.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_TYPE_DOMAIN_VISIBLE_PASSWORD"></a><a id="cred_type_domain_visible_password"></a><dl>
<dt><b><b>CRED_TYPE_DOMAIN_VISIBLE_PASSWORD</b></b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
This value is no longer supported.

<b>Windows Server 2003 and Windows XP:  </b>The credential is a password credential and is specific to authentication packages from Microsoft. The Passport authentication package will automatically use this credential when connecting to the named target.

Additional values will be defined in the future. Applications should be written to allow for credential types they do not understand.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_TYPE_GENERIC_CERTIFICATE"></a><a id="cred_type_generic_certificate"></a><dl>
<dt><b>CRED_TYPE_GENERIC_CERTIFICATE</b></dt>
<dt>5 (0x5)</dt>
</dl>
</td>
<td width="60%">
The credential is  a certificate credential that is a generic authentication package. 

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_TYPE_DOMAIN_EXTENDED"></a><a id="cred_type_domain_extended"></a><dl>
<dt><b>CRED_TYPE_DOMAIN_EXTENDED</b></dt>
<dt>6 (0x6)</dt>
</dl>
</td>
<td width="60%">
The credential is supported by extended Negotiate packages.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_TYPE_MAXIMUM"></a><a id="cred_type_maximum"></a><dl>
<dt><b>CRED_TYPE_MAXIMUM</b></dt>
<dt>7 (0x7)</dt>
</dl>
</td>
<td width="60%">
The maximum number of supported credential types.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_TYPE_MAXIMUM_EX"></a><a id="cred_type_maximum_ex"></a><dl>
<dt><b>CRED_TYPE_MAXIMUM_EX</b></dt>
<dt>CRED_TYPE_MAXIMUM+1000</dt>
</dl>
</td>
<td width="60%">
The extended maximum number of supported credential types that now allow new applications to run on older operating systems.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -field TargetName

The name of the credential. The <b>TargetName</b> and <b>Type</b> members uniquely identify the credential. This member cannot be changed after the credential is created. Instead, the credential with the old name should be deleted and the credential with the new name created.

If <b>Type</b> is <b>CRED_TYPE_DOMAIN_PASSWORD</b> or <b>CRED_TYPE_DOMAIN_CERTIFICATE</b>, this member identifies the server or servers that the credential is to be used for. The member is either a NetBIOS or DNS server name, a DNS host name suffix that contains a wildcard character, a NetBIOS or DNS domain name that contains a wildcard character sequence, or an asterisk.

If <b>TargetName</b> is a DNS host name, the <b>TargetAlias</b> member can be the NetBIOS name of the host.

If the <b>TargetName</b> is  a DNS host name suffix that contains a wildcard character, the leftmost label of the DNS host name is an asterisk (*), which denotes that the target name is any server whose name ends in the specified name, for example, *.microsoft.com.

If the <b>TargetName</b> is a domain name that contains a wildcard character sequence, the syntax is the domain name followed by a backslash and asterisk (\*), which denotes that the target name is any server that is a member of the named domain (or realm).

If <b>TargetName</b> is a DNS domain name that contains a wildcard character sequence, the <b>TargetAlias</b> member can be a NetBIOS domain name that uses a wildcard sequence for the same domain.



If <b>TargetName</b>  specifies a DFS share, for example, <i>DfsRoot</i><b>\\</b><i>DfsShare</i>, then this credential matches the specific DFS share and any servers reached through that DFS share.


If <b>TargetName</b> is a single asterisk (*), this credential matches any server name.

If <b>TargetName</b> is CRED_SESSION_WILDCARD_NAME, this credential matches any server name. This credential matches before a single asterisk and is only valid if <b>Persist</b> is <b>CRED_PERSIST_SESSION</b>. The credential can be set by applications that want to temporarily override the default credential.

This member cannot be longer than <b>CRED_MAX_DOMAIN_TARGET_NAME_LENGTH</b> (337) characters.

If the <b>Type</b> is CRED_TYPE_GENERIC, this member should identify the service that uses the credential in addition to the actual target. Microsoft suggests the name be prefixed by the name of the company implementing the service. Microsoft will use the prefix "Microsoft". Services written by Microsoft should append their service name, for example <b>Microsoft_RAS_</b><i>TargetName</i>. This member cannot be longer than <b>CRED_MAX_GENERIC_TARGET_NAME_LENGTH</b> (32767) characters.

This member is case-insensitive.

### -field Comment

A string comment from the user that describes this credential. This member cannot be longer than <b>CRED_MAX_STRING_LENGTH</b> (256) characters.

### -field LastWritten

The time, in Coordinated Universal Time (Greenwich Mean Time), of the last modification of the credential. For write operations, the value of this member is ignored.

### -field CredentialBlobSize

The size, in bytes, of the <b>CredentialBlob</b> member. This member cannot be larger than <b>CRED_MAX_CREDENTIAL_BLOB_SIZE</b> (5*512) bytes.

### -field CredentialBlob

Secret data for the credential. The <b>CredentialBlob</b> member can be both read and written.

If the <b>Type</b> member is <b>CRED_TYPE_DOMAIN_PASSWORD</b>, this member contains the plaintext Unicode password for <b>UserName</b>. The <b>CredentialBlob</b> and <b>CredentialBlobSize</b> members do not include a trailing zero character. Also, for <b>CRED_TYPE_DOMAIN_PASSWORD</b>, this member can only be read by the authentication packages.

If the <b>Type</b> member is <b>CRED_TYPE_DOMAIN_CERTIFICATE</b>, this member contains the clear test Unicode PIN for <b>UserName</b>. The <b>CredentialBlob</b> and <b>CredentialBlobSize</b> members do not include a trailing zero character. Also, this member can only be read by the authentication packages.

If the <b>Type</b> member is <b>CRED_TYPE_GENERIC</b>, this member is defined by the application.

Credentials are expected to be portable. Applications should ensure that the data in <b>CredentialBlob</b> is portable. The application defines the byte-endian and alignment of the data in <b>CredentialBlob</b>.

### -field Persist

Defines the persistence of this credential. This member can be read and written.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRED_PERSIST_SESSION"></a><a id="cred_persist_session"></a><dl>
<dt><b><b>CRED_PERSIST_SESSION</b></b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The credential persists for the life of the logon session. It will not be visible to other logon sessions of this same user. It will not exist after this user logs off and back on.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_PERSIST_LOCAL_MACHINE"></a><a id="cred_persist_local_machine"></a><dl>
<dt><b><b>CRED_PERSIST_LOCAL_MACHINE</b></b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The credential persists for all subsequent logon sessions on this same computer. It is visible to other logon sessions of this same user on this same computer and not visible to logon sessions for this user on other computers.

<b>Windows Vista Home Basic, Windows Vista Home Premium, Windows Vista Starter and Windows XP Home Edition:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_PERSIST_ENTERPRISE"></a><a id="cred_persist_enterprise"></a><dl>
<dt><b><b>CRED_PERSIST_ENTERPRISE</b></b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
The credential persists for all subsequent logon sessions on this same computer. It is visible to other logon sessions of this same user on this same computer and to logon sessions for this user on other computers.

This option can be implemented as locally persisted credential if the administrator or user configures the user account to not have roam-able state. For instance, if the user has no roaming profile, the credential will only persist locally.

<b>Windows Vista Home Basic, Windows Vista Home Premium, Windows Vista Starter and Windows XP Home Edition:  </b>This value is not supported.

</td>
</tr>
</table>

### -field AttributeCount

The number of application-defined attributes to be associated with the credential. This member can be read and written. Its value cannot be greater than <b>CRED_MAX_ATTRIBUTES</b> (64).

### -field Attributes

Application-defined attributes that are associated with the credential. This member can be read and written.

### -field TargetAlias

Alias for the <b>TargetName</b> member. This member can be read and written. It cannot be longer than <b>CRED_MAX_STRING_LENGTH</b> (256) characters.

If the credential <b>Type</b> is <b>CRED_TYPE_GENERIC</b>, this member can be non-<b>NULL</b>, but the credential manager ignores the member.

### -field UserName

The user name of the account used to connect to <b>TargetName</b>. 




If the credential <b>Type</b> is <b>CRED_TYPE_DOMAIN_PASSWORD</b>, this member can be either a <i>DomainName</i><b></b><i>UserName</i> or a UPN.

If the credential <b>Type</b> is <b>CRED_TYPE_DOMAIN_CERTIFICATE</b>, this member must be a marshaled certificate reference created by calling <a href="/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a> with a CertCredential.

If the credential <b>Type</b> is <b>CRED_TYPE_GENERIC</b>, this member can be non-<b>NULL</b>, but the credential manager ignores the member.

This member cannot be longer than <b>CRED_MAX_USERNAME_LENGTH</b> (513) characters.

## -remarks

> [!NOTE]
> The wincred.h header defines CREDENTIAL as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).