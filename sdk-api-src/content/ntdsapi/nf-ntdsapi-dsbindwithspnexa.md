---
UID: NF:ntdsapi.DsBindWithSpnExA
title: DsBindWithSpnExA function (ntdsapi.h)
description: Binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication. (DsBindWithSpnExA)
helpviewer_keywords: ["DsBindWithSpnExA", "NTDSAPI_BIND_ALLOW_DELEGATION", "NTDSAPI_BIND_FIND_BINDING", "NTDSAPI_BIND_FORCE_KERBEROS", "ntdsapi/DsBindWithSpnExA"]
old-location: ad\dsbindwithspnex.htm
tech.root: ad
ms.assetid: 52a5761d-5244-4bc9-8c09-fd08f10a9fff
ms.date: 12/05/2018
ms.keywords: DsBindWithSpnEx, DsBindWithSpnEx function [Active Directory], DsBindWithSpnExA, DsBindWithSpnExW, NTDSAPI_BIND_ALLOW_DELEGATION, NTDSAPI_BIND_FIND_BINDING, NTDSAPI_BIND_FORCE_KERBEROS, ad.dsbindwithspnex, ntdsapi/DsBindWithSpnEx, ntdsapi/DsBindWithSpnExA, ntdsapi/DsBindWithSpnExW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsBindWithSpnExW (Unicode) and DsBindWithSpnExA (ANSI)
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
 - DsBindWithSpnExA
 - ntdsapi/DsBindWithSpnExA
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
 - API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
 - KernelBase.dll
api_name:
 - DsBindWithSpnEx
 - DsBindWithSpnExA
 - DsBindWithSpnExW
---

# DsBindWithSpnExA function


## -description

The <b>DsBindWithSpnEx</b> function binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication. This function is similar to the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a> function except this function allows more binding options with the <i>BindFlags</i> parameter.

This function is provided where complete control is required over mutual authentication. Do not use this function if you expect <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> to find a server for you, because SPNs are computer-specific, and it is unlikely that the SPN you provide will match the server that <b>DsBind</b> finds for you. Providing a <b>NULL</b><i>ServicePrincipalName</i> argument results in behavior that is identical to <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>.

## -parameters

### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind. For more information, see the <i>DomainControllerName</i> description in the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.

### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind. For more information, see the <i>DnsDomainName</i> description in the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.

### -param AuthIdentity [in, optional]

Contains an <a href="/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a> value that represents the credentials to be used for the bind. The 
    
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a> function is used to obtain this value. If this parameter is <b>NULL</b>,
    the credentials of the calling thread are used.


<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> must be called before freeing this handle with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a> function.

### -param ServicePrincipalName [in, optional]

Pointer to a null-terminated string that specifies the Service Principal Name to assign to the client. Passing <b>NULL</b> in <i>ServicePrincipalName</i> is equivalent to a call to the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a> function.

### -param BindFlags [in, optional]

Contains a set of flags that define the behavior of this function. This parameter can contain zero or a combination of the values listed in the following list.



#### NTDSAPI_BIND_ALLOW_DELEGATION (1)

Causes the bind to use the delegate impersonation level. This allows operations that require delegation, such as
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsaddsidhistorya">DsAddSidHistory</a>, to succeed.  Specifying this flag also causes <b>DsBindWithSpnEx</b> to operate like <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a>.

If this flag is not specified, the bind will use the impersonate impersonation level. For more information, see <a href="/windows/desktop/com/impersonation-levels">Impersonation Levels</a>.

Most operations do
not require the delegate impersonation level, so this flag should only be specified 
if  absolutely required. Binding to a rogue server with the  delegate impersonation level will allow the rogue server to connect to a non-rogue server with your credentials and perform
unintended operations.



#### NTDSAPI_BIND_FIND_BINDING (2)

Reserved.



#### NTDSAPI_BIND_FORCE_KERBEROS (4)

<b>Active Directory Lightweight Directory Services:  </b>If this flag is specified, <b>DsBindWithSpnEx</b> forces Kerberos authentication to be used. If Kerberos authentication cannot be established, <b>DsBindWithSpnEx</b> will not attempt to authenticate with any other method.

### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> function.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following list lists common error codes.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a>



<a href="/windows/desktop/com/impersonation-levels">Impersonation Levels</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsBindWithSpnEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
