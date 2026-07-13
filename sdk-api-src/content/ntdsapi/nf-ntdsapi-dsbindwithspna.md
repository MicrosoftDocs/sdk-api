---
UID: NF:ntdsapi.DsBindWithSpnA
title: DsBindWithSpnA function (ntdsapi.h)
description: Binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication. (DsBindWithSpnA)
helpviewer_keywords: ["DsBindWithSpnA", "ntdsapi/DsBindWithSpnA"]
old-location: ad\dsbindwithspn.htm
tech.root: ad
ms.assetid: 9a149654-fd94-4b0c-b712-07fb827bef2f
ms.date: 12/05/2018
ms.keywords: DsBindWithSpn, DsBindWithSpn function [Active Directory], DsBindWithSpnA, DsBindWithSpnW, _glines_dsbindwithspn, ad.dsbindwithspn, ntdsapi/DsBindWithSpn, ntdsapi/DsBindWithSpnA, ntdsapi/DsBindWithSpnW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsBindWithSpnW (Unicode) and DsBindWithSpnA (ANSI)
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
 - DsBindWithSpnA
 - ntdsapi/DsBindWithSpnA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsBindWithSpn
 - DsBindWithSpnA
 - DsBindWithSpnW
---

# DsBindWithSpnA function


## -description

The <b>DsBindWithSpn</b> function binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication.

This function is provided for where complete control is required for mutual authentication. Do not use this function if you expect <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> to find a server for you, because SPNs are computer-specific, and it is unlikely that the SPN you provide will match the server that <b>DsBind</b> finds for you. Providing a <b>NULL</b><i>ServicePrincipalName</i> argument results in behavior that is identical to <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>.

## -parameters

### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information, see the <i>DomainControllerName</i> description in the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.

### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information, see the <i>DnsDomainName</i> description in the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.

### -param AuthIdentity [in, optional]

Contains an <a href="/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a> value that represents the credentials to be used for the bind. The 
    
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a> function is used to obtain this value. If this parameter is <b>NULL</b>,
    the credentials of the calling thread are used.


<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> must be called before freeing this handle with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a> function.

### -param ServicePrincipalName [in, optional]

Pointer to a null-terminated string that specifies the Service Principal Name to assign to the client. Passing <b>NULL</b> in <i>ServicePrincipalName</i> is equivalent to a call to the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a> function.

### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> function.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following are the most common error codes.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsBindWithSpn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
