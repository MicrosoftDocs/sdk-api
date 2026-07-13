---
UID: NF:ntdsapi.DsMakePasswordCredentialsA
title: DsMakePasswordCredentialsA function (ntdsapi.h)
description: Constructs a credential handle suitable for use with the DsBindWithCred function. (ANSI)
helpviewer_keywords: ["DsMakePasswordCredentialsA", "ntdsapi/DsMakePasswordCredentialsA"]
old-location: ad\dsmakepasswordcredentials.htm
tech.root: ad
ms.assetid: 51aba58b-07c5-4e6d-8568-fa6f1a963d8e
ms.date: 12/05/2018
ms.keywords: DsMakePasswordCredentials, DsMakePasswordCredentials function [Active Directory], DsMakePasswordCredentialsA, DsMakePasswordCredentialsW, _glines_dsmakepasswordcredentials, ad.dsmakepasswordcredentials, ntdsapi/DsMakePasswordCredentials, ntdsapi/DsMakePasswordCredentialsA, ntdsapi/DsMakePasswordCredentialsW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsMakePasswordCredentialsW (Unicode) and DsMakePasswordCredentialsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsMakePasswordCredentialsA
 - ntdsapi/DsMakePasswordCredentialsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
 - API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
 - DsMakePasswordCredentials
 - DsMakePasswordCredentialsA
 - DsMakePasswordCredentialsW
---

# DsMakePasswordCredentialsA function


## -description

The <b>DsMakePasswordCredentials</b> function constructs a credential handle suitable for use with the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a> function.

## -parameters

### -param User [in]

Pointer to a null-terminated string that contains the user name to use for the credentials.

### -param Domain [in]

Pointer to a null-terminated string that contains the domain that the user is a member of.

### -param Password [in]

Pointer to a null-terminated string that contains the password to use for the credentials.

### -param pAuthIdentity [out]

Pointer to an <a href="/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a> value that receives the credential handle. This handle is used in a subsequent call to <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>.   This handle must be freed with the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a> function when it is no longer required.

## -returns

Returns a Windows error code, including the following.

## -remarks

A null, default credential handle is created if <i>User</i>, <i>Domain</i> and <i>Password</i> are all <b>NULL</b>. Otherwise, <i>User</i> must be present. The <i>Domain</i> parameter may be <b>NULL</b> when <i>User</i> is fully qualified, such as a user in UPN format; for example, "someone@fabrikam.com".

When the handle returned in <i>pAuthIdentity</i> is passed to <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>, <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> must be called before freeing the handle with <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a>.  The normal sequence is:

<ol>
<li>Call <b>DsMakePasswordCredentials</b> to obtain the credential handle.</li>
<li>Call <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>, and pass the credential handle.</li>
<li>Call <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnbind</a> when the binding is no longer required.</li>
<li>Call <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a> to free the credential handle.</li>
</ol>




> [!NOTE]
> The ntdsapi.h header defines DsMakePasswordCredentials as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnbind</a>



<a href="/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a>
