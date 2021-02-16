---
UID: NC:ntsecpkg.LSA_ADD_CREDENTIAL
title: LSA_ADD_CREDENTIAL (ntsecpkg.h)
description: Adds credentials to a logon session.
helpviewer_keywords: ["AddCredential","AddCredential callback function [Security]","LSA_ADD_CREDENTIAL","LSA_ADD_CREDENTIAL callback","_lsa_addcredential","ntsecpkg/AddCredential","security.addcredential"]
old-location: security\addcredential.htm
tech.root: security
ms.assetid: ea6ddd18-818e-43f5-9453-de2b3f994325
ms.date: 12/05/2018
ms.keywords: AddCredential, AddCredential callback function [Security], LSA_ADD_CREDENTIAL, LSA_ADD_CREDENTIAL callback, _lsa_addcredential, ntsecpkg/AddCredential, security.addcredential
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_ADD_CREDENTIAL
 - ntsecpkg/LSA_ADD_CREDENTIAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - AddCredential
---

# LSA_ADD_CREDENTIAL callback function


## -description

<p class="CCE_Message">[<b>AddCredential</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications should use the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function with <b>KerbAddExtraCredentialsMessage</b> specified as the message type. <b>KerbAddExtraCredentialsMessage</b> is a   <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration value.]

Adds credentials to a logon session. These credentials can later be referenced  through a call to the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_credentials">GetCredentials</a> function.

## -parameters

### -param LogonId [in]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> that contains the session ID of the logon session to which credentials are to be added.

### -param AuthenticationPackage [in]

The authentication package ID of the calling authentication package. This value is received in the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_initialize_package">LsaApInitializePackage</a> call during DLL initialization.

### -param PrimaryKeyValue [in]

A string that contains a value that the authentication package will later need to reference as a primary key of the credential data. This can be used, for example, to keep the name of the domain or server the credentials are related to. The format and meaning of this string are specific to the authentication package. Note that the string value does not have to be unique, even for the specified logon session. For example, there can be two passwords for the same domain, each with the passwords stored as credentials and the domain name stored as the primary key.

### -param Credentials [in]

A string that represents the user credentials. The format and meaning of this string are specific to the authentication package.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code, which can be the following value or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

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
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an <b>NTSTATUS</b> code to a Windows error code.

## -remarks

The body of the credential string must be self-relative; that is, it must contain no pointers to memory outside the credentials. Credentials are copied, and any pointers outside the credentials themselves will no longer be valid in the copy. In particular, strings referred to in credentials should have both the UNICODE_STRING header and body placed in the credential buffer. Pointers to strings in the body of credentials should be changed to offsets.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_credentials">GetCredentials</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>