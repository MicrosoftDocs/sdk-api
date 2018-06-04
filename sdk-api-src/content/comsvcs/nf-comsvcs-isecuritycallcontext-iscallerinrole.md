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

# ISecurityCallContext::IsCallerInRole


## -description


Determines whether the direct caller is in the specified role.


## -parameters




### -param bstrRole [in]

The name of the role.


### -param pfInRole [out]

<b>TRUE</b> if the caller is in the specified role; <b>FALSE</b> if not. If the specified role is not defined for the application, <b>FALSE</b> is returned. This parameter is set to <b>TRUE</b> if role-based security is not enabled.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The role specified in the <i>bstrRole</i> parameter is a recognized role, and the Boolean result returned in the <i>pfIsInRole</i> parameter indicates whether the caller is in that role.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_ROLENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The role specified in the <i>bstrRole</i> parameter does not exist.

</td>
</tr>
</table>
 




## -remarks



Use this method to limit access to sections of code that should not be executed unless the caller is a member of the specified role. Windows groups and users are assigned to an application's roles using the Component Services administration tool. For more information about roles, see <a href="https://msdn.microsoft.com/7247758e-f486-4ce2-afca-f0d10fffe626">Role-Based Security</a>.

<b>IsCallerInRole</b> only applies to the direct caller of the currently executing method. <b>IsCallerInRole</b> does not apply to any other caller in the call sequence from which the current method was called. However, you can obtain information about other callers in the sequence by using the <a href="https://msdn.microsoft.com/e6561b89-8af6-46cc-aeab-2b007d48fe26">get_Item</a> property method to get the Callers property of the security call context object.

Because <b>IsCallerInRole</b> is <b>TRUE</b> when role-based security is not enabled, it is a good idea to call <a href="https://msdn.microsoft.com/b247d430-56b1-40be-a85a-5ed141d90c85">IsSecurityEnabled</a> before calling <b>IsCallerInRole</b> to ensure that <b>IsCallerInRole</b> returns useful information. 





## -see-also




<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>



<a href="https://msdn.microsoft.com/6117970c-5dbd-485e-978e-3aa96e42b359">Programmatic Component Security</a>



<a href="https://msdn.microsoft.com/7247758e-f486-4ce2-afca-f0d10fffe626">Role-Based Security</a>
 

 

