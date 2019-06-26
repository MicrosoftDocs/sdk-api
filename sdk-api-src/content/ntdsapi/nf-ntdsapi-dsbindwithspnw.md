---
UID: NF:ntdsapi.DsBindWithSpnW
title: DsBindWithSpnW function (ntdsapi.h)
author: windows-sdk-content
description: Binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication.
old-location: ad\dsbindwithspn.htm
tech.root: ad
ms.assetid: 9a149654-fd94-4b0c-b712-07fb827bef2f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsBindWithSpn, DsBindWithSpn function [Active Directory], DsBindWithSpnA, DsBindWithSpnW, _glines_dsbindwithspn, ad.dsbindwithspn, ntdsapi/DsBindWithSpn, ntdsapi/DsBindWithSpnA, ntdsapi/DsBindWithSpnW
ms.topic: function
f1_keywords: 
 - "ntdsapi/DsBindWithSpn"
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsBindWithSpnW function


## -description


The <b>DsBindWithSpn</b> function binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication.

This function is provided for where complete control is required for mutual authentication. Do not use this function if you expect <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> to find a server for you, because SPNs are computer-specific, and it is unlikely that the SPN you provide will match the server that <b>DsBind</b> finds for you. Providing a <b>NULL</b><i>ServicePrincipalName</i> argument results in behavior that is identical to <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>.


## -parameters




### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information, see the <i>DomainControllerName</i> description in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.


### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information, see the <i>DnsDomainName</i> description in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.


### -param AuthIdentity [in, optional]

Contains an <a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a> value that represents the credentials to be used for the bind. The 
    
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a>function is used to obtain this value. If this parameter is <b>NULL</b>,
    the credentials of the calling thread are used.


<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> must be called before freeing this handle with the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a> function.


### -param ServicePrincipalName [in, optional]

Pointer to a null-terminated string that specifies the Service Principal Name to assign to the client. Passing <b>NULL</b> in <i>ServicePrincipalName</i> is equivalent to a call to the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a> function.


### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> function.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following are the most common error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a>
 

 

