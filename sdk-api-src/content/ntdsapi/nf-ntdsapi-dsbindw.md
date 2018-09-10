---
UID: NF:ntdsapi.DsBindW
title: DsBindW function
author: windows-sdk-content
description: Binds to a domain controller.
old-location: ad\dsbind.htm
tech.root: ad
ms.assetid: c73cd16d-ccfd-4f61-b1c5-50130bef64d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DsBind, DsBind function [Active Directory], DsBindA, DsBindW, _glines_dsbind, ad.dsbind, ntdsapi/DsBind, ntdsapi/DsBindA, ntdsapi/DsBindW
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
req.unicode-ansi: DsBindW (Unicode) and DsBindA (ANSI)
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
 - DsBind
 - DsBindA
 - DsBindW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsBindW function


## -description


The <b>DsBind</b> function binds to a domain controller.<b>DsBind</b> uses the default process credentials to bind to the domain controller. To specify alternate credentials, use the 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a> function.


## -parameters




### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the name of the domain controller to bind to. This name can be the name of the domain controller or the fully qualified DNS name of the domain controller. Either name type can, optionally, be preceded by two backslash characters. All of the following examples represent correctly formatted domain controller names:

<ul>
<li>"FAB-DC-01"</li>
<li>"\\FAB-DC-01"</li>
<li>"FAB-DC-01.fabrikam.com"</li>
<li>"\\FAB-DC-01.fabrikam.com"</li>
</ul>
This parameter can be <b>NULL</b>. For more information, see Remarks.


### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. This parameter can be <b>NULL</b>. For more  information, see Remarks.


### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a> function.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following are the most common error codes.




## -remarks



The behavior of the 
    <b>DsBind</b> function is determined by the contents of the <i>DomainControllerName</i> and <i>DnsDomainName</i> parameters. The following list describes the behavior of this function based on the contents of these parameters.

<table>
<tr>
<th><i>DomainControllerName</i></th>
<th><i>DnsDomainName</i></th>
<th>Description</th>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>DsBind</b> will attempt to bind to a global catalog server in the forest of the local computer.

</td>
</tr>
<tr>
<td>
(value)

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>DsBind</b> will attempt to bind to the domain controller specified by the  <i>DomainControllerName</i> parameter.

</td>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
(value)

</td>
<td>
<b>DsBind</b> will attempt to bind to any domain controller in the domain specified by <i>DnsDomainName</i> parameter.

</td>
</tr>
<tr>
<td>
(value</p>)</td>
<td>
(value)

</td>
<td>
The <i>DomainControllerName</i> parameter takes precedence. <b>DsBind</b> will attempt to bind to the domain controller specified by the  <i>DomainControllerName</i> parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0c09fe26-ef53-48b1-8ac2-70ccb8f3e3e2">DOMAIN_CONTROLLER_INFO</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a>
 

 

