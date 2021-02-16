---
UID: NF:comsvcs.ObjectContext.IsSecurityEnabled
title: ObjectContext::IsSecurityEnabled (comsvcs.h)
description: Indicates whether security is enabled for the current object.
helpviewer_keywords: ["IsSecurityEnabled","IsSecurityEnabled method [COM+]","IsSecurityEnabled method [COM+]","ObjectContext interface","ObjectContext interface [COM+]","IsSecurityEnabled method","ObjectContext.IsSecurityEnabled","ObjectContext::IsSecurityEnabled","_cos_ObjectContext_IsSecurityEnabled","comsvcs/ObjectContext::IsSecurityEnabled","cos.objectcontext_issecurityenabled"]
old-location: cos\objectcontext_issecurityenabled.htm
tech.root: cos
ms.assetid: c7b3a301-9f94-40de-a3d2-5387fb4e0596
ms.date: 12/05/2018
ms.keywords: IsSecurityEnabled, IsSecurityEnabled method [COM+], IsSecurityEnabled method [COM+],ObjectContext interface, ObjectContext interface [COM+],IsSecurityEnabled method, ObjectContext.IsSecurityEnabled, ObjectContext::IsSecurityEnabled, _cos_ObjectContext_IsSecurityEnabled, comsvcs/ObjectContext::IsSecurityEnabled, cos.objectcontext_issecurityenabled
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
 - ObjectContext::IsSecurityEnabled
 - comsvcs/ObjectContext::IsSecurityEnabled
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
 - ObjectContext.IsSecurityEnabled
---

# ObjectContext::IsSecurityEnabled


## -description

Indicates whether security is enabled for the current object.

## -parameters

### -param pbIsEnabled [out]

<b>TRUE</b> if security is enabled for this object; <b>FALSE</b> otherwise.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-issecurityenabled">IsSecurityEnabled</a> using this pointer. An <b>ObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>

## -remarks

In the COM+ environment, server and library applications can use role-based security. <b>IsSecurityEnabled</b> returns <b>TRUE</b> when an application uses role-based security, and role-based security is enabled both for the application and the specific component that called the method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>