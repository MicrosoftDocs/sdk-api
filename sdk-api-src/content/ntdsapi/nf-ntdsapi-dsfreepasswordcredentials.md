---
UID: NF:ntdsapi.DsFreePasswordCredentials
title: DsFreePasswordCredentials function
author: windows-sdk-content
description: Frees memory allocated for a credentials structure by the DsMakePasswordCredentials function.
old-location: ad\dsfreepasswordcredentials.htm
tech.root: ad
ms.assetid: 3d008aa8-feff-426f-911b-a447257076c2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DsFreePasswordCredentials, DsFreePasswordCredentials function [Active Directory], _glines_dsfreepasswordcredentials, ad.dsfreepasswordcredentials, ntdsapi/DsFreePasswordCredentials
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
req.unicode-ansi: 
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
 - API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
 - DsFreePasswordCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsFreePasswordCredentials function


## -description


The <b>DsFreePasswordCredentials</b> function frees memory allocated for a credentials structure by the 
<a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a> function.


## -parameters




### -param AuthIdentity [in]

Handle of the credential structure to be freed.


## -returns



This function does not return a value.




## -remarks



When the handle  in <i>AuthIdentity</i> is passed to <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>, <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnbind</a> must be called before freeing this handle. The normal sequence of events is:

<ol>
<li>Call <a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a> to obtain the credential handle.</li>
<li>Call <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>, passing the credential handle.</li>
<li>Call <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnbind</a> when the RPC connection is no longer required.</li>
<li>Call <b>DsFreePasswordCredentials</b> to free the credential handle.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a>



<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnbind</a>
 

 

