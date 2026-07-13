---
UID: NF:comsvcs.ObjectContext.IsCallerInRole
title: ObjectContext::IsCallerInRole (comsvcs.h)
description: Indicates whether the object's direct caller is in a specified role (either directly or as part of a group). (ObjectContext.IsCallerInRole)
helpviewer_keywords: ["IsCallerInRole","IsCallerInRole method [COM+]","IsCallerInRole method [COM+]","ObjectContext interface","ObjectContext interface [COM+]","IsCallerInRole method","ObjectContext.IsCallerInRole","ObjectContext::IsCallerInRole","_cos_ObjectContext_IsCallerInRole","comsvcs/ObjectContext::IsCallerInRole","cos.objectcontext_iscallerinrole"]
old-location: cos\objectcontext_iscallerinrole.htm
tech.root: cos
ms.assetid: e1ef03e6-fcb2-463b-b2b3-a88e958a1d19
ms.date: 12/05/2018
ms.keywords: IsCallerInRole, IsCallerInRole method [COM+], IsCallerInRole method [COM+],ObjectContext interface, ObjectContext interface [COM+],IsCallerInRole method, ObjectContext.IsCallerInRole, ObjectContext::IsCallerInRole, _cos_ObjectContext_IsCallerInRole, comsvcs/ObjectContext::IsCallerInRole, cos.objectcontext_iscallerinrole
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
 - ObjectContext::IsCallerInRole
 - comsvcs/ObjectContext::IsCallerInRole
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
 - ObjectContext.IsCallerInRole
---

# ObjectContext::IsCallerInRole


## -description

Indicates whether the object's direct caller is in a specified role (either directly or as part of a group).

## -parameters

### -param bstrRole [in]

The name of the role.

### -param pbInRole [out]

<b>TRUE</b> if the caller is in the specified role; <b>FALSE</b> otherwise. This parameter is also set to <b>TRUE</b> if security is not enabled.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

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
The role specified in the <i>bstrRole</i> parameter is a recognized role, and the Boolean result returned in the <i>pbIsInRole</i> parameter indicates whether the caller is in that role.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_ROLENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The role specified in the bstrRole parameter does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-iscallerinrole">IsCallerInRole</a> using this pointer. An <b>ObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>

## -remarks

Use this method to determine whether the direct caller of the currently executing method is associated with a specific role. A role is a symbolic name that represents a user or group of users who have specific access permissions to all components in a given COM+ application. Developers define roles when they create a component, and roles are mapped to individual users or groups at deployment time.

<b>IsCallerInRole</b> applies only to the direct caller of the currently executing method. (The direct caller is the process calling into the current server process. It can be either a base client process or a server process.) <b>IsCallerInRole</b> does not apply to the process that initiated the call sequence from which the current method was called or to any other callers in that sequence.

Because <b>IsCallerInRole</b> returns <b>TRUE</b> when the object that invokes it is executing in a client's process, it is a good idea to call <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-issecurityenabled">IsSecurityEnabled</a> before calling <b>IsCallerInRole</b>. If security isn't enabled, <b>IsCallerInRole</b> will not return an accurate result.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>
