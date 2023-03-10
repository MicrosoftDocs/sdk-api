---
UID: NF:comsvcs.IObjectContext.IsCallerInRole
title: IObjectContext::IsCallerInRole (comsvcs.h)
description: Indicates whether the object's direct caller is in a specified role (either directly or as part of a group). (IObjectContext.IsCallerInRole)
helpviewer_keywords: ["IObjectContext interface [COM+]","IsCallerInRole method","IObjectContext.IsCallerInRole","IObjectContext::IsCallerInRole","IsCallerInRole","IsCallerInRole method [COM+]","IsCallerInRole method [COM+]","IObjectContext interface","_cos_IObjectContext_IsCallerInRole","comsvcs/IObjectContext::IsCallerInRole","cos.iobjectcontext_iscallerinrole"]
old-location: cos\iobjectcontext_iscallerinrole.htm
tech.root: cos
ms.assetid: 8e545cc5-ad4e-43b9-a834-c9d470df24dd
ms.date: 12/05/2018
ms.keywords: IObjectContext interface [COM+],IsCallerInRole method, IObjectContext.IsCallerInRole, IObjectContext::IsCallerInRole, IsCallerInRole, IsCallerInRole method [COM+], IsCallerInRole method [COM+],IObjectContext interface, _cos_IObjectContext_IsCallerInRole, comsvcs/IObjectContext::IsCallerInRole, cos.iobjectcontext_iscallerinrole
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
 - IObjectContext::IsCallerInRole
 - comsvcs/IObjectContext::IsCallerInRole
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
 - IObjectContext.IsCallerInRole
---

# IObjectContext::IsCallerInRole


## -description

Indicates whether the object's direct caller is in a specified role (either directly or as part of a group).

## -parameters

### -param bstrRole [in]

The name of the role.

### -param pfIsInRole [out]

<b>TRUE</b> if the caller is in the specified role; <b>FALSE</b> if not. This parameter is also set to <b>TRUE</b> if security is not enabled.

## -returns

This method can return the following values.

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
The role specified in the <i>bstrRole</i> parameter does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments passed in is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-iscallerinrole">IsCallerInRole</a> using this pointer. An <b>IObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>

## -remarks

You use this method to determine whether the direct caller of the currently executing method is associated with a specific role. A role is a symbolic name that represents a user or group of users who have specific access permissions to all components in a given COM+ application. Developers define roles when they create a component, and roles are mapped to individual users or groups at deployment time.

<b>IsCallerInRole</b> applies only to the direct caller of the currently executing method. (The direct caller is the process calling into the current server process. It can be either a base client process or a server process.) <b>IsCallerInRole</b> does not apply to the process that initiated the call sequence from which the current method was called or to any other callers in that sequence.

Because <b>IsCallerInRole</b> returns <b>TRUE</b> when the object that invokes it is executing in a client's process, it's a good idea to call <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-issecurityenabled">IsSecurityEnabled</a> before calling <b>IsCallerInRole</b>. If security isn't enabled, <b>IsCallerInRole</b> will not return an accurate result.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
