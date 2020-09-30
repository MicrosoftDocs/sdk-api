---
UID: NC:ntsecpkg.LSA_DELETE_CREDENTIAL
title: LSA_DELETE_CREDENTIAL (ntsecpkg.h)
description: Deletes an existing credential.
helpviewer_keywords: ["DeleteCredential","DeleteCredential callback function [Security]","LSA_DELETE_CREDENTIAL","LSA_DELETE_CREDENTIAL callback","_lsa_deletecredential","ntsecpkg/DeleteCredential","security.deletecredential"]
old-location: security\deletecredential.htm
tech.root: security
ms.assetid: 06bc02ec-5c07-41db-9f00-49773a597a09
ms.date: 12/05/2018
ms.keywords: DeleteCredential, DeleteCredential callback function [Security], LSA_DELETE_CREDENTIAL, LSA_DELETE_CREDENTIAL callback, _lsa_deletecredential, ntsecpkg/DeleteCredential, security.deletecredential
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
 - LSA_DELETE_CREDENTIAL
 - ntsecpkg/LSA_DELETE_CREDENTIAL
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
 - DeleteCredential
---

# LSA_DELETE_CREDENTIAL callback function


## -description

Deletes an existing credential.

This function deletes the first credential it finds with a matching logon session ID, authentication package ID, and primary lookup key value. If there are multiple matching credentials, only one of them is deleted.

This function is not used by newer authentication packages, such as Kerberos.

## -parameters

### -param LogonId [in]

Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure containing the session ID of the logon session from which the credential is to be deleted.

### -param AuthenticationPackage [in]

Authentication package ID of the calling authentication package received in the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_initialize_package">LsaApInitializePackage</a> call during DLL initialization.

### -param PrimaryKeyValue [in]

Contains the primary lookup key of the credential to be deleted.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
No matching credential could be found.

</td>
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
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>