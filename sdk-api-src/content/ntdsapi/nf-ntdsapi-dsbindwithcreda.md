---
UID: NF:ntdsapi.DsBindWithCredA
title: DsBindWithCredA function
author: windows-driver-content
description: Binds to a domain controller using the specified credentials.
old-location: ad\dsbindwithcred.htm
old-project: AD
ms.assetid: 708e3874-852c-4a57-bf4b-edaf98818fe5
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: DsBindWithCred, DsBindWithCred function [Active Directory], DsBindWithCredA, DsBindWithCredW, _glines_dsbindwithcred, ad.dsbindwithcred, ntdsapi/DsBindWithCred, ntdsapi/DsBindWithCredA, ntdsapi/DsBindWithCredW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: DS_REPL_OP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
api_name:
-	DsBindWithCred
-	DsBindWithCredA
-	DsBindWithCredW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DsBindWithCredA function


## -description


The <b>DsBindWithCred</b> function
  binds to a domain controller using the specified credentials.


## -parameters




### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind. For more information about this parameter, see the <i>DomainControllerName</i> description in the <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> topic.


### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. For more information about this parameter, see the <i>DnsDomainName</i> description in the <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> topic.

This parameter is required to secure a Kerberos authentication.


### -param AuthIdentity [in, optional]

Contains an <a href="https://msdn.microsoft.com/06e45348-a392-45be-9f8a-e77ef887f26c">RPC_AUTH_IDENTITY_HANDLE</a> value that represents the credentials to be used for the bind. The 
    
<a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a>
    function is used to obtain this value. If this parameter is <b>NULL</b>,
    the credentials of the calling thread are used.


<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a> must be called before freeing this handle with the <a href="https://msdn.microsoft.com/3d008aa8-feff-426f-911b-a447257076c2">DsFreePasswordCredentials</a> function.


### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a> function.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following are the most common error codes.




## -see-also




<a href="https://msdn.microsoft.com/0c09fe26-ef53-48b1-8ac2-70ccb8f3e3e2">DOMAIN_CONTROLLER_INFO</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/3d008aa8-feff-426f-911b-a447257076c2">DsFreePasswordCredentials</a>



<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a>



<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a>



<a href="https://msdn.microsoft.com/775dd350-5c70-4d97-aa2f-d21e9aecc778">Mutual
    Authentication Using Kerberos</a>
 

 

