---
UID: NF:wincred.CredUnPackAuthenticationBufferW
title: CredUnPackAuthenticationBufferW function
author: windows-sdk-content
description: Converts an authentication buffer returned by a call to the CredUIPromptForWindowsCredentials function into a string user name and password.
old-location: security\credunpackauthenticationbuffer.htm
tech.root: secauthn
ms.assetid: c87f0b11-59c2-4450-ad63-398cdb15016f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CredUnPackAuthenticationBuffer, CredUnPackAuthenticationBuffer function [Security], CredUnPackAuthenticationBufferA, CredUnPackAuthenticationBufferW, security.credunpackauthenticationbuffer, wincred/CredUnPackAuthenticationBuffer, wincred/CredUnPackAuthenticationBufferA, wincred/CredUnPackAuthenticationBufferW
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
req.unicode-ansi: CredUnPackAuthenticationBufferW (Unicode) and CredUnPackAuthenticationBufferA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CredUnPackAuthenticationBufferW function


## -description


The <b>CredUnPackAuthenticationBuffer</b> function converts an authentication buffer returned by a call to the <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> function into a string user name and password.


## -parameters




### -param dwFlags [in]

Setting the value of this parameter to <b>CRED_PACK_PROTECTED_CREDENTIALS</b> specifies that the function attempts to decrypt the credentials in the authentication buffer. If the credential  cannot be decrypted, the function returns <b>FALSE</b>, and a call to the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function will return the value <b>ERROR_NOT_CAPABLE</b>.

How the decryption is done depends on the format of the authentication buffer.

If the authentication buffer is a <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure, the function can decrypt the buffer if it is encrypted by using <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a> with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option.

If the authentication buffer is one of the marshaled KERB_*_LOGON structures, the function decrypts the password before returning it in the <i>pszPassword</i> buffer.


### -param pAuthBuffer [in]

A pointer to the authentication buffer to be converted.

This buffer is typically the output of the <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> or <a href="https://msdn.microsoft.com/48ffdd7a-1969-4f6a-bbc7-2826e21ea052">CredPackAuthenticationBuffer</a> function. This must be one of the following types:<ul>
<li>A <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure for identity credentials. The function does not accept other <a href="https://msdn.microsoft.com/a9c9471b-2134-4173-af86-18b277627d2a">SEC_WINNT_AUTH_IDENTITY</a> structures.</li>
<li>A <a href="https://msdn.microsoft.com/96aec0cc-b3e1-4b4b-aa0e-ecf05b9fabbe">KERB_INTERACTIVE_LOGON</a> or <a href="https://msdn.microsoft.com/211d89e9-36a6-4177-8eea-d01eca320718">KERB_INTERACTIVE_UNLOCK_LOGON</a>  structure for password credentials.</li>
<li>A <a href="https://msdn.microsoft.com/e6aa0042-edb5-4e9b-b545-5159d3bfb8fc">KERB_CERTIFICATE_LOGON</a> or <a href="https://msdn.microsoft.com/04e058b0-9a05-4ed7-9d4a-1c8c003d8077">KERB_CERTIFICATE_UNLOCK_LOGON</a>  structure for smart card certificate credentials.</li>
<li>GENERIC_CRED for generic credentials.</li>
</ul>



### -param cbAuthBuffer [in]

The size, in bytes, of the <i>pAuthBuffer</i> buffer.


### -param pszUserName [out]

A pointer to a null-terminated string that receives the user name.

This string can be a marshaled credential. See Remarks.


#### - pcchMaxUserName [in, out]

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. The following table shows common values for the <b>GetLastError</b> function.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_NOT_CAPABLE</b></b></dt>
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
<dt><b><b>ERROR_INSUFFICIENT_BUFFER</b></b></dt>
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
<dt><b><b>ERROR_NOT_SUPPORTED</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The authentication buffer is not of a supported type.

</td>
</tr>
</table>
 




## -remarks



Beginning with  Windows 8 and Windows Server 2012, the authentication buffer can be a <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure, which can be optionally encrypted by using the <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option. This credential format is returned by a Credential Provider of an Identity Provider by using the <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> or <a href="https://msdn.microsoft.com/2af2ac00-0e91-4384-9ffa-3e100df218c1">SspiPromptForCredentials</a> function. This structure can also be constructed by using the <a href="https://msdn.microsoft.com/48ffdd7a-1969-4f6a-bbc7-2826e21ea052">CredPackAuthenticationBuffer</a> function. 
If the authentication buffer <i>pAuthBuffer</i> represents a nonpassword credential, such as <a href="https://msdn.microsoft.com/e6aa0042-edb5-4e9b-b545-5159d3bfb8fc">KERB_CERTIFICATE_LOGON</a> or <b>SEC_WINNT_AUTH_IDENTITY_EX2</b>, the function must marshal the credential as character strings, returned as user name, domain name, and password strings. The marshaling is done by using a specific procedure. When <i>dwFlags</i> contains the CRED_PACK_PROTECTED_CREDENTIALS flag, the caller must run in the same logon session in which the credential was encrypted.




