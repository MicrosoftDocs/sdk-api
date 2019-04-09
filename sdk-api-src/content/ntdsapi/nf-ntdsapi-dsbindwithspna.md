---
UID: NF:ntdsapi.DsBindWithSpnA
title: DsBindWithSpnA function (ntdsapi.h)
author: windows-sdk-content
description: Binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication.
old-location: ad\dsbindwithspn.htm
tech.root: ad
ms.assetid: 9a149654-fd94-4b0c-b712-07fb827bef2f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsBindWithSpn, DsBindWithSpn function [Active Directory], DsBindWithSpnA, DsBindWithSpnW, _glines_dsbindwithspn, ad.dsbindwithspn, ntdsapi/DsBindWithSpn, ntdsapi/DsBindWithSpnA, ntdsapi/DsBindWithSpnW
ms.topic: function
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
---

# DsBindWithSpnA function


## -description


The <b>DsBindWithSpn</b> function binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication.

This function is provided for where complete control is required for mutual authentication. Do not use this function if you expect <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> to find a server for you, because SPNs are computer-specific, and it is unlikely that the SPN you provide will match the server that <b>DsBind</b> finds for you. Providing a <b>NULL</b><i>ServicePrincipalName</i> argument results in behavior that is identical to <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>.


## -parameters




### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information, see the <i>DomainControllerName</i> description in the <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> topic.


### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information, see the <i>DnsDomainName</i> description in the <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> topic.


### -param AuthIdentity [in, optional]

Contains an <a href="https://msdn.microsoft.com/06e45348-a392-45be-9f8a-e77ef887f26c">RPC_AUTH_IDENTITY_HANDLE</a> value that represents the credentials to be used for the bind. The 
    
<a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a>function is used to obtain this value. If this parameter is <b>NULL</b>,
    the credentials of the calling thread are used.


<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a> must be called before freeing this handle with the <a href="https://msdn.microsoft.com/3d008aa8-feff-426f-911b-a447257076c2">DsFreePasswordCredentials</a> function.


### -param ServicePrincipalName [in, optional]

Pointer to a null-terminated string that specifies the Service Principal Name to assign to the client. Passing <b>NULL</b> in <i>ServicePrincipalName</i> is equivalent to a call to the <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a> function.


### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a> function.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following are the most common error codes.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a>
 

 

