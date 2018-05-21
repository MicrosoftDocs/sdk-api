---
UID: NF:wincred.CredPackAuthenticationBufferA
title: CredPackAuthenticationBufferA function
author: windows-driver-content
description: Converts a string user name and password into an authentication buffer.
old-location: security\credpackauthenticationbuffer.htm
old-project: SecAuthN
ms.assetid: 48ffdd7a-1969-4f6a-bbc7-2826e21ea052
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CRED_PACK_GENERIC_CREDENTIALS, CRED_PACK_ID_PROVIDER_CREDENTIALS, CRED_PACK_PROTECTED_CREDENTIALS, CRED_PACK_WOW_BUFFER, CredPackAuthenticationBuffer, CredPackAuthenticationBuffer function [Security], CredPackAuthenticationBufferA, CredPackAuthenticationBufferW, security.credpackauthenticationbuffer, wincred/CredPackAuthenticationBuffer, wincred/CredPackAuthenticationBufferA, wincred/CredPackAuthenticationBufferW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredPackAuthenticationBufferW (Unicode) and CredPackAuthenticationBufferA (ANSI)
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
-	Credui.dll
-	Ext-MS-Win-security-credui-l1-1-0.dll
-	Ext-MS-Win-security-credui-l1-1-1.dll
-	AnalogCredUI.dll
api_name:
-	CredPackAuthenticationBuffer
-	CredPackAuthenticationBufferA
-	CredPackAuthenticationBufferW
product: Windows
targetos: Windows
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CredPackAuthenticationBufferA function


## -description


The <b>CredPackAuthenticationBuffer</b> function converts a string user name and password into an authentication buffer.

Beginning with Windows 8 and Windows Server 2012, the <b>CredPackAuthenticationBuffer</b> function converts an identity credential into an authentication buffer, which is a <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure. This buffer can be passed to <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>, <a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle</a>, or other identity provider interfaces.


## -parameters




### -param dwFlags [in]

Specifies how the credential should be packed. This can be a combination of the following flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRED_PACK_PROTECTED_CREDENTIALS"></a><a id="cred_pack_protected_credentials"></a><dl>
<dt><b>CRED_PACK_PROTECTED_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
Encrypts the credential so that it can only be decrypted by processes in the caller's logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_PACK_WOW_BUFFER"></a><a id="cred_pack_wow_buffer"></a><dl>
<dt><b>CRED_PACK_WOW_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Encrypts the credential in a WOW buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_PACK_GENERIC_CREDENTIALS"></a><a id="cred_pack_generic_credentials"></a><dl>
<dt><b>CRED_PACK_GENERIC_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
Encrypts the credential in a CRED_GENERIC buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_PACK_ID_PROVIDER_CREDENTIALS"></a><a id="cred_pack_id_provider_credentials"></a><dl>
<dt><b>CRED_PACK_ID_PROVIDER_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
 Encrypts the credential of an online identity into a <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure.  If CRED_PACK_GENERIC_CREDENTIALS and CRED_PACK_ID_PROVIDER_CREDENTIALS are not set, encrypts the credentials in a KERB_INTERACTIVE_LOGON buffer.

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008:  </b>This value is not supported.

</td>
</tr>
</table>
 


### -param pszUserName [in]

A pointer to a null-terminated string that specifies the user name to be converted. For domain users, the string must be in the following format:

<i>DomainName</i><b>\</b><i>UserName</i>

For online identities, if the credential is a plaintext password, the user name format is <i>ProviderName</i><b>\</b><i>UserName</i>. If the credential is a <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure, the user name is an encoded string that is the <i>UserName</i> parameter output of a function call to <a href="https://msdn.microsoft.com/0610a7b8-67e9-4c01-893f-da579eeea2f8">SspiEncodeAuthIdentityAsStrings</a>.

For <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> or certificate credentials, the user name is an encoded string that is the output of a function call to <a href="https://msdn.microsoft.com/20a1d54b-04a7-4b0a-88e4-1970d1f71502">CredMarshalCredential</a> with the CertCredential option.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>Online identities are not supported.


### -param pszPassword [in]

A pointer to a null-terminated string that specifies the password to be converted.

For <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> credentials, the password is an encoded string that is in the <i>ppszPackedCredentialsString</i> output of a function call to <a href="https://msdn.microsoft.com/0610a7b8-67e9-4c01-893f-da579eeea2f8">SspiEncodeAuthIdentityAsStrings</a>.

For <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a>  credentials, this is the <i>smart card</i> PIN.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>Online identities are not supported.


### -param pPackedCredentials [out]

A pointer to an array of bytes that, on output, receives the packed authentication buffer. This parameter can be <b>NULL</b> to receive the required buffer size in the <i>pcbPackedCredentials</i> parameter.


### -param pcbPackedCredentials [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the <i>pPackedCredentials</i> buffer. On output, if the buffer is not of sufficient size, specifies the required size, in bytes, of the  <i>pPackedCredentials</i> buffer.


## -returns



<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.

For extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function, which may return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer provided by <i>pPackedCredentials</i> is too small.

</td>
</tr>
</table>
 



