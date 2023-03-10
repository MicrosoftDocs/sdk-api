---
UID: NF:comsvcs.ISecurityCallContext.IsCallerInRole
title: ISecurityCallContext::IsCallerInRole (comsvcs.h)
description: Determines whether the direct caller is in the specified role.
helpviewer_keywords: ["ISecurityCallContext interface [COM+]","IsCallerInRole method","ISecurityCallContext.IsCallerInRole","ISecurityCallContext::IsCallerInRole","IsCallerInRole","IsCallerInRole method [COM+]","IsCallerInRole method [COM+]","ISecurityCallContext interface","_cos_ISecurityCallContext_IsCallerInRole","comsvcs/ISecurityCallContext::IsCallerInRole","cos.isecuritycallcontext_iscallerinrole"]
old-location: cos\isecuritycallcontext_iscallerinrole.htm
tech.root: cos
ms.assetid: 544deb46-6427-4936-97a6-ea995b5e77ba
ms.date: 12/05/2018
ms.keywords: ISecurityCallContext interface [COM+],IsCallerInRole method, ISecurityCallContext.IsCallerInRole, ISecurityCallContext::IsCallerInRole, IsCallerInRole, IsCallerInRole method [COM+], IsCallerInRole method [COM+],ISecurityCallContext interface, _cos_ISecurityCallContext_IsCallerInRole, comsvcs/ISecurityCallContext::IsCallerInRole, cos.isecuritycallcontext_iscallerinrole
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityCallContext::IsCallerInRole
 - comsvcs/ISecurityCallContext::IsCallerInRole
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityCallContext.IsCallerInRole
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

Use this method to limit access to sections of code that should not be executed unless the caller is a member of the specified role. Windows groups and users are assigned to an application's roles using the Component Services administration tool. For more information about roles, see <a href="/windows/desktop/cossdk/role-based-security-administration">Role-Based Security</a>.

<b>IsCallerInRole</b> only applies to the direct caller of the currently executing method. <b>IsCallerInRole</b> does not apply to any other caller in the call sequence from which the current method was called. However, you can obtain information about other callers in the sequence by using the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-get_item">get_Item</a> property method to get the Callers property of the security call context object.

Because <b>IsCallerInRole</b> is <b>TRUE</b> when role-based security is not enabled, it is a good idea to call <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled">IsSecurityEnabled</a> before calling <b>IsCallerInRole</b> to ensure that <b>IsCallerInRole</b> returns useful information.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>



<a href="/windows/desktop/cossdk/programmatic-component-security">Programmatic Component Security</a>



<a href="/windows/desktop/cossdk/role-based-security-administration">Role-Based Security</a>