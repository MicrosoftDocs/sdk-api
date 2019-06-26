---
UID: NF:ntdsapi.DsBindWithCredA
title: DsBindWithCredA function (ntdsapi.h)
author: windows-sdk-content
description: Binds to a domain controller using the specified credentials.
old-location: ad\dsbindwithcred.htm
tech.root: ad
ms.assetid: 708e3874-852c-4a57-bf4b-edaf98818fe5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsBindWithCred, DsBindWithCred function [Active Directory], DsBindWithCredA, DsBindWithCredW, _glines_dsbindwithcred, ad.dsbindwithcred, ntdsapi/DsBindWithCred, ntdsapi/DsBindWithCredA, ntdsapi/DsBindWithCredW
ms.topic: function
f1_keywords: 
 - "ntdsapi/DsBindWithCred"
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsBindWithCredA function


## -description


The <b>DsBindWithCred</b> function
  binds to a domain controller using the specified credentials.


## -parameters




### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind. For more information about this parameter, see the <i>DomainControllerName</i> description in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.


### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information about this parameter, see the <i>DnsDomainName</i> description in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> topic.

This parameter is required to secure a Kerberos authentication.


### -param AuthIdentity [in, optional]

Contains an <a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a> value that represents the credentials to be used for the bind. The 
    
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a>function is used to obtain this value. If this parameter is <b>NULL</b>,
    the credentials of the calling thread are used.


<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> must be called before freeing this handle with the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a> function.


### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> function.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following are the most common error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dsgetdc/ns-dsgetdc-_domain_controller_infoa">DOMAIN_CONTROLLER_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreepasswordcredentials">DsFreePasswordCredentials</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/mutual-authentication-using-kerberos">Mutual
    Authentication Using Kerberos</a>
 

 

