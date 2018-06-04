---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DsServerRegisterSpnA function


## -description


The <b>DsServerRegisterSpn</b> function composes two SPNs for a host-based service. The names are based on the DNS and NetBIOS names of the local computer. The function modifies the <b>servicePrincipalName</b> attribute of either a specified account or of the account associated with the calling thread. The function either registers or unregisters the SPNs.

A host-based service is a service instance that provides services identified with its host computer, as distinguished from a replicable service where clients have no preference which host computer a service instance runs on.


## -parameters




### -param Operation [in]

Specifies what operation <b>DsServerRegisterSpn</b> should perform. This parameter can have one of the following values.



#### DS_SPN_ADD_SPN_OP

Adds the SPNs to the user or computer account.



#### DS_SPN_DELETE_SPN_OP

Deletes the specified SPNs from the account.



#### DS_SPN_REPLACE_SPN_OP

Removes all SPNs currently registered on the user or computer account and replaces them with the new SPNs.


### -param ServiceClass [in]

Pointer to a constant null-terminated string specifying the class of the service. This parameter may be any string unique to that service; either the protocol name (for example, ldap) or the string form of a GUID will work.


### -param UserObjectDN [in, optional]

Pointer to a constant null-terminated string specifying the distinguished name of a user or computer account object to write the SPNs to. If this parameter is <b>NULL</b>, <b>DsServerRegisterSpn</b> writes to the account object of the primary or impersonated user associated with the calling thread. If the thread is running in the security context of the LocalSystem account, the function writes to the account object of the local computer.


## -returns



If the function successfully registers one or more SPNs, it returns <b>ERROR_SUCCESS</b>. Modification is performed permissively, so that adding a value that already exists does not return an error.




## -remarks



The two SPNs composed by the <b>DsServerRegisterSpn</b> function have the following format:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>&lt;ServiceClass&gt;/&lt;host&gt;</pre>
</td>
</tr>
</table></span></div>
In one SPN, the host computer is the fully qualified DNS name of the local computer. In the other SPN, the host component is the NetBIOS name of the local computer.

In most cases, the <b>DsServerRegisterSpn</b> caller must have domain administrator privileges to successfully modify the <b>servicePrincipalName</b> attribute of an account object. The exception to this rule is if the calling thread is running under the LocalSystem account, <b>DsServerRegisterSpn</b> is allowed if the <i>UserObjectDN</i> parameter is either <b>NULL</b> or specifies the distinguished name of the local computer account.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/cbd53850-9b05-4f74-ab07-30dcad583fc5">DsGetSpn</a>



<a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a>
 

 

