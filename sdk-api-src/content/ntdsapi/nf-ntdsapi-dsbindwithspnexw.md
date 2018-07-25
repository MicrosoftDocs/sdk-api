---
UID: NF:ntdsapi.DsBindWithSpnExW
title: DsBindWithSpnExW function
author: windows-sdk-content
description: Binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication.
old-location: ad\dsbindwithspnex.htm
old-project: ad
ms.assetid: 52a5761d-5244-4bc9-8c09-fd08f10a9fff
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: DsBindWithSpnEx, DsBindWithSpnEx function [Active Directory], DsBindWithSpnExA, DsBindWithSpnExW, NTDSAPI_BIND_ALLOW_DELEGATION, NTDSAPI_BIND_FIND_BINDING, NTDSAPI_BIND_FORCE_KERBEROS, ad.dsbindwithspnex, ntdsapi/DsBindWithSpnEx, ntdsapi/DsBindWithSpnExA, ntdsapi/DsBindWithSpnExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DS_REPL_OP_TYPE
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
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: ADAM
---

# DsBindWithSpnExW function


## -description


The <b>DsBindWithSpnEx</b> function binds to a domain controller using the specified credentials and a specific service principal name (SPN) for mutual authentication. This function is similar to the <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a> function except this function allows more binding options with the <i>BindFlags</i> parameter.

This function is provided where complete control is required over mutual authentication. Do not use this function if you expect <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> to find a server for you, because SPNs are computer-specific, and it is unlikely that the SPN you provide will match the server that <b>DsBind</b> finds for you. Providing a <b>NULL</b><i>ServicePrincipalName</i> argument results in behavior that is identical to <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>.


## -parameters




### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind. For more information, see the <i>DomainControllerName</i> description in the <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> topic.


### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind. For more information, see the <i>DnsDomainName</i> description in the <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a> topic.


### -param AuthIdentity [in, optional]

Contains an <a href="https://msdn.microsoft.com/06e45348-a392-45be-9f8a-e77ef887f26c">RPC_AUTH_IDENTITY_HANDLE</a> value that represents the credentials to be used for the bind. The 
    
<a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a>
    function is used to obtain this value. If this parameter is <b>NULL</b>,
    the credentials of the calling thread are used.


<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a> must be called before freeing this handle with the <a href="https://msdn.microsoft.com/3d008aa8-feff-426f-911b-a447257076c2">DsFreePasswordCredentials</a> function.


### -param ServicePrincipalName [in, optional]

Pointer to a null-terminated string that specifies the Service Principal Name to assign to the client. Passing <b>NULL</b> in <i>ServicePrincipalName</i> is equivalent to a call to the <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a> function.


### -param BindFlags [in, optional]

Contains a set of flags that define the behavior of this function. This parameter can contain zero or a combination of the values listed in the following list.



#### NTDSAPI_BIND_ALLOW_DELEGATION (1)

Causes the bind to use the delegate impersonation level. This allows operations that require delegation, such as
<a href="https://msdn.microsoft.com/36ef8734-717a-4c3a-a839-6591d85c9734">DsAddSidHistory</a>, to succeed.  Specifying this flag also causes <b>DsBindWithSpnEx</b> to operate like <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>.

If this flag is not specified, the bind will use the impersonate impersonation level. For more information, see <a href="https://msdn.microsoft.com/library/ms686632(v=VS.85).aspx">Impersonation Levels</a>.

Most operations do
not require the delegate impersonation level, so this flag should only be specified 
if  absolutely required. Binding to a rogue server with the  delegate impersonation level will allow the rogue server to connect to a non-rogue server with your credentials and perform
unintended operations.



#### NTDSAPI_BIND_FIND_BINDING (2)

Reserved.



#### NTDSAPI_BIND_FORCE_KERBEROS (4)

<b>Active Directory Lightweight Directory Services:  </b>If this flag is specified, <b>DsBindWithSpnEx</b> forces Kerberos authentication to be used. If Kerberos authentication cannot be established, <b>DsBindWithSpnEx</b> will not attempt to authenticate with any other method.


### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a> function.


##### - BindFlags.NTDSAPI_BIND_ALLOW_DELEGATION (1)

Causes the bind to use the delegate impersonation level. This allows operations that require delegation, such as
<a href="https://msdn.microsoft.com/36ef8734-717a-4c3a-a839-6591d85c9734">DsAddSidHistory</a>, to succeed.  Specifying this flag also causes <b>DsBindWithSpnEx</b> to operate like <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>.

If this flag is not specified, the bind will use the impersonate impersonation level. For more information, see <a href="https://msdn.microsoft.com/library/ms686632(v=VS.85).aspx">Impersonation Levels</a>.

Most operations do
not require the delegate impersonation level, so this flag should only be specified 
if  absolutely required. Binding to a rogue server with the  delegate impersonation level will allow the rogue server to connect to a non-rogue server with your credentials and perform
unintended operations.


##### - BindFlags.NTDSAPI_BIND_FIND_BINDING (2)

Reserved.


##### - BindFlags.NTDSAPI_BIND_FORCE_KERBEROS (4)

<b>Active Directory Lightweight Directory Services:  </b>If this flag is specified, <b>DsBindWithSpnEx</b> forces Kerberos authentication to be used. If Kerberos authentication cannot be established, <b>DsBindWithSpnEx</b> will not attempt to authenticate with any other method.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following list lists common error codes.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>



<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a>



<a href="https://msdn.microsoft.com/library/ms686632(v=VS.85).aspx">Impersonation Levels</a>
 

 

