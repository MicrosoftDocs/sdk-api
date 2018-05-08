---
UID: NF:comsvcs.ISecurityCallContext.IsUserInRole
title: ISecurityCallContext::IsUserInRole
author: windows-driver-content
description: Determines whether the specified user is in the specified role.
old-location: cos\isecuritycallcontext_isuserinrole.htm
old-project: cossdk
ms.assetid: aae5d89a-be46-40c8-ad5d-21f9b3a9c04f
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ISecurityCallContext interface [COM+],IsUserInRole method, ISecurityCallContext.IsUserInRole, ISecurityCallContext::IsUserInRole, IsUserInRole, IsUserInRole method [COM+], IsUserInRole method [COM+],ISecurityCallContext interface, _cos_ISecurityCallContext_IsUserInRole, comsvcs/ISecurityCallContext::IsUserInRole, cos.isecuritycallcontext_isuserinrole
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ISecurityCallContext.IsUserInRole
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISecurityCallContext::IsUserInRole


## -description


Determines whether the specified user is in the specified role.


## -parameters




### -param pUser [in]

A pointer to value holding the User ID of the user whose role membership is to be checked. If you intend to pass the security identifier (SID) to <b>IsUserInRole</b>, this parameter should meet the following requirements: <code>V_VT(pUser) == (VT_ARRAY|VT_UI1) &amp;&amp; V_ARRAY(pUser)-&gt;cDims == 1</code>.


### -param bstrRole [in]

The name of the role.


### -param pfInRole [out]

<b>TRUE</b> if the user is in the specified role; <b>FALSE</b> if not. If the specified role is not defined for the application, <b>FALSE</b> is returned. This parameter is set to <b>TRUE</b> if role-based security is not enabled.


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
The role specified in the <i>bstrRole</i> parameter is a recognized role, and the Boolean result returned in the <i>pfIsInRole</i> parameter indicates whether the user is in that role.

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

Because <b>IsUserInRole</b> is <b>TRUE</b> when role-based security is not enabled, it is a good idea to call <a href="https://msdn.microsoft.com/b247d430-56b1-40be-a85a-5ed141d90c85">IsSecurityEnabled</a> before calling <b>IsUserInRole</b> to ensure that <b>IsUserInRole</b> returns useful information.




## -see-also




<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>



<a href="https://msdn.microsoft.com/6117970c-5dbd-485e-978e-3aa96e42b359">Programmatic Component Security</a>
 

 

