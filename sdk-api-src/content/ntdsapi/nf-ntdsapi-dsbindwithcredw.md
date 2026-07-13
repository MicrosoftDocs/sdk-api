---
UID: NF:ntdsapi.DsBindWithCredW
title: DsBindWithCredW function (ntdsapi.h)
description: Binds to a domain controller using the specified credentials. (Unicode)
helpviewer_keywords: ["DsBindWithCred", "DsBindWithCred function [Active Directory]", "DsBindWithCredW", "_glines_dsbindwithcred", "ad.dsbindwithcred", "ntdsapi/DsBindWithCred", "ntdsapi/DsBindWithCredW"]
old-location: ad\dsbindwithcred.htm
tech.root: ad
ms.assetid: 708e3874-852c-4a57-bf4b-edaf98818fe5
ms.date: 12/05/2018
ms.keywords: DsBindWithCred, DsBindWithCred function [Active Directory], DsBindWithCredA, DsBindWithCredW, _glines_dsbindwithcred, ad.dsbindwithcred, ntdsapi/DsBindWithCred, ntdsapi/DsBindWithCredA, ntdsapi/DsBindWithCredW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsBindWithCredW (Unicode) and DsBindWithCredA (ANSI)
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
 - DsBindWithCredW
 - ntdsapi/DsBindWithCredW
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
 - DsBindWithCred
 - DsBindWithCredA
 - DsBindWithCredW
---

# DsBindWithCredW function


## -description

The <b>DsBindWithCred</b> function
  binds to a domain controller using the specified credentials.

## -parameters

### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind. For more information about this parameter, see the <i>DomainControllerName</i> description in the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.

### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information about this parameter, see the <i>DnsDomainName</i> description in the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.

This parameter is required to secure a Kerberos authentication.

### -param AuthIdentity [in, optional]

Contains an <a href="/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a> value that represents the credentials to be used for the bind. The 
    
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a> function is used to obtain this value. If this parameter is <b>NULL</b>,
    the credentials of the calling thread are used.


<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> must be called before freeing this handle with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a> function.

### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> function.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following are the most common error codes.

## -see-also

<a href="/windows/desktop/api/dsgetdc/ns-dsgetdc-domain_controller_infoa">DOMAIN_CONTROLLER_INFO</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a>



<a href="/windows/desktop/AD/mutual-authentication-using-kerberos">Mutual
    Authentication Using Kerberos</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsBindWithCred as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
