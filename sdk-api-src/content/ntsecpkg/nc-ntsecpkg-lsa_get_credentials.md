---
UID: NC:ntsecpkg.LSA_GET_CREDENTIALS
title: LSA_GET_CREDENTIALS (ntsecpkg.h)
description: Retrieves credentials associated with a logon session.
helpviewer_keywords: ["GetCredentials","GetCredentials callback function [Security]","LSA_GET_CREDENTIALS","LSA_GET_CREDENTIALS callback","_lsa_getcredentials","ntsecpkg/GetCredentials","security.getcredentials"]
old-location: security\getcredentials.htm
tech.root: security
ms.assetid: e9a2d112-6681-4400-b316-ffd7095e319a
ms.date: 12/05/2018
ms.keywords: GetCredentials, GetCredentials callback function [Security], LSA_GET_CREDENTIALS, LSA_GET_CREDENTIALS callback, _lsa_getcredentials, ntsecpkg/GetCredentials, security.getcredentials
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
 - LSA_GET_CREDENTIALS
 - ntsecpkg/LSA_GET_CREDENTIALS
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
 - GetCredentials
---

# LSA_GET_CREDENTIALS callback function


## -description

Retrieves credentials associated with a logon session.

This function is not used by newer authentication packages, such as Kerberos.

## -parameters

### -param LogonId [in]

Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure containing the session ID of the logon session from which credentials are to be retrieved.

### -param AuthenticationPackage [in]

Authentication package ID of the calling authentication package. Authentication packages should retrieve only their own credentials.

### -param QueryContext [in, out]

Pointer to an unsigned <b>LONG</b> value used across successive calls to retrieve multiple credentials. The first time this function is used, the value pointed to by this argument should be zero. Thereafter, this value will be updated to allow retrieval to continue where it left off. This value should, therefore, not be changed until all credentials of a given query operation have been retrieved.

### -param RetrieveAllCredentials [in]

Indicates whether all credentials for the specified logon session should be retrieved (<b>TRUE</b>), or only those matching the specified <i>PrimaryKeyValue</i> (<b>FALSE</b>).

### -param PrimaryKeyValue [in, out]

This parameter serves two purposes. If the <i>RetrieveAllCredentials</i> parameter is <b>FALSE</b>, this string contains the value to use as a primary lookup key. In this case, only credentials belonging to the correct logon session with a primary lookup key matching this value will be retrieved. 




If <i>RetrieveAllCredentials</i> is <b>TRUE</b>, the value of this string on input is ignored and the primary lookup key of each credential retrieved is returned in this string.

### -param PrimaryKeyLength [out]

If the <i>RetrieveAllCredentials</i> parameter is <b>TRUE</b>, this parameter receives the length needed to store the <i>PrimaryKeyValue</i> string.

### -param Credentials [out]

Pointer to a buffer that receives the retrieved credential. Only one credential is retrieved for each call made. The credential is returned in a buffer that the function allocates by calling the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateLsaHeap</a> function. It is the caller's responsibility to free the <i>Credentials</i> buffer when it is no longer needed, by calling 
<a href="/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap">FreeLsaHeap</a>.

## -returns

If the function succeeds, the function returns the NTSTATUS code, STATUS_SUCCESS, indicating that the credentials were successfully retrieved.

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
No more credentials are available. If this code is returned on the first call, there are no credentials matching the selection criteria.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
The string provided to receive the <i>PrimaryKeyValue</i> was not large enough to hold the data. In this case, no data is retrieved, and the <i>QueryContext</i> value is not modified. This allows the same call to be made again with a larger string buffer.

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