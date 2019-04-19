---
UID: NC:ntsecpkg.LSA_ADD_CREDENTIAL
title: LSA_ADD_CREDENTIAL (ntsecpkg.h)
author: windows-sdk-content
description: Adds credentials to a logon session.
old-location: security\addcredential.htm
tech.root: SecAuthN
ms.assetid: ea6ddd18-818e-43f5-9453-de2b3f994325
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddCredential, AddCredential callback function [Security], LSA_ADD_CREDENTIAL, LSA_ADD_CREDENTIAL callback, _lsa_addcredential, ntsecpkg/AddCredential, security.addcredential
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - AddCredential
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_ADD_CREDENTIAL callback function


## -description


<p class="CCE_Message">[<b>AddCredential</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications should use the <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function with <b>KerbAddExtraCredentialsMessage</b> specified as the message type. <b>KerbAddExtraCredentialsMessage</b> is a   <a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration value.]

Adds credentials to a logon session. These credentials can later be referenced  through a call to the 
<a href="https://msdn.microsoft.com/e9a2d112-6681-4400-b316-ffd7095e319a">GetCredentials</a> function.


## -parameters




### -param LogonId [in]

A pointer to an 
<a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> that contains the session ID of the logon session to which credentials are to be added.


### -param AuthenticationPackage [in]

The authentication package ID of the calling authentication package. This value is received in the 
<a href="https://msdn.microsoft.com/1fed5a5e-5dc1-4b59-aa28-bd1395a27742">LsaApInitializePackage</a> call during DLL initialization.


### -param PrimaryKeyValue [in]

A string that contains a value that the authentication package will later need to reference as a primary key of the credential data. This can be used, for example, to keep the name of the domain or server the credentials are related to. The format and meaning of this string are specific to the authentication package. Note that the string value does not have to be unique, even for the specified logon session. For example, there can be two passwords for the same domain, each with the passwords stored as credentials and the domain name stored as the primary key.


### -param Credentials [in]

A string that represents the user credentials. The format and meaning of this string are specific to the authentication package.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code, which can be the following value or one of the 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_LOGON_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The specified logon session could not be found.

</td>
</tr>
</table>
 

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an <b>NTSTATUS</b> code to a Windows error code.




## -remarks



The body of the credential string must be self-relative; that is, it must contain no pointers to memory outside the credentials. Credentials are copied, and any pointers outside the credentials themselves will no longer be valid in the copy. In particular, strings referred to in credentials should have both the UNICODE_STRING header and body placed in the credential buffer. Pointers to strings in the body of credentials should be changed to offsets.




## -see-also




<a href="https://msdn.microsoft.com/e9a2d112-6681-4400-b316-ffd7095e319a">GetCredentials</a>



<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

