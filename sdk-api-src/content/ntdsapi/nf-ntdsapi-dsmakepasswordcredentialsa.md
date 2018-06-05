---
UID: NF:ntdsapi.DsMakePasswordCredentialsA
title: DsMakePasswordCredentialsA function
author: windows-sdk-content
description: Constructs a credential handle suitable for use with the DsBindWithCred function.
old-location: ad\dsmakepasswordcredentials.htm
old-project: AD
ms.assetid: 51aba58b-07c5-4e6d-8568-fa6f1a963d8e
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DsMakePasswordCredentials, DsMakePasswordCredentials function [Active Directory], DsMakePasswordCredentialsA, DsMakePasswordCredentialsW, _glines_dsmakepasswordcredentials, ad.dsmakepasswordcredentials, ntdsapi/DsMakePasswordCredentials, ntdsapi/DsMakePasswordCredentialsA, ntdsapi/DsMakePasswordCredentialsW
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
req.unicode-ansi: DsMakePasswordCredentialsW (Unicode) and DsMakePasswordCredentialsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DS_REPL_OP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
-	API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
-	KernelBase.dll
-	API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
-	DsMakePasswordCredentials
-	DsMakePasswordCredentialsA
-	DsMakePasswordCredentialsW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DsMakePasswordCredentialsA function


## -description


The <b>DsMakePasswordCredentials</b> function constructs a credential handle suitable for use with the 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a> function.


## -parameters




### -param User [in]

Pointer to a null-terminated string that contains the user name to use for the credentials.


### -param Domain [in]

Pointer to a null-terminated string that contains the domain that the user is a member of.


### -param Password [in]

Pointer to a null-terminated string that contains the password to use for the credentials.


### -param pAuthIdentity [out]

Pointer to an <a href="https://msdn.microsoft.com/06e45348-a392-45be-9f8a-e77ef887f26c">RPC_AUTH_IDENTITY_HANDLE</a> value that receives the credential handle. This handle is used in a subsequent call to <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>.   This handle must be freed with the 
<a href="https://msdn.microsoft.com/3d008aa8-feff-426f-911b-a447257076c2">DsFreePasswordCredentials</a> function when it is no longer required.


## -returns



Returns a Windows error code, including the following.




## -remarks



A null, default credential handle is created if <i>User</i>, <i>Domain</i> and <i>Password</i> are all <b>NULL</b>. Otherwise, <i>User</i> must be present. The <i>Domain</i> parameter may be <b>NULL</b> when <i>User</i> is fully qualified, such as a user in UPN format; for example, "someone@fabrikam.com".

When the handle returned in <i>pAuthIdentity</i> is passed to <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>, <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a> must be called before freeing the handle with <a href="https://msdn.microsoft.com/3d008aa8-feff-426f-911b-a447257076c2">DsFreePasswordCredentials</a>.  The normal sequence is:

<ol>
<li>Call <b>DsMakePasswordCredentials</b> to obtain the credential handle.</li>
<li>Call <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>, and pass the credential handle.</li>
<li>Call <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnbind</a> when the binding is no longer required.</li>
<li>Call <a href="https://msdn.microsoft.com/3d008aa8-feff-426f-911b-a447257076c2">DsFreePasswordCredentials</a> to free the credential handle.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/3d008aa8-feff-426f-911b-a447257076c2">DsFreePasswordCredentials</a>



<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnbind</a>



<a href="https://msdn.microsoft.com/06e45348-a392-45be-9f8a-e77ef887f26c">RPC_AUTH_IDENTITY_HANDLE</a>
 

 

