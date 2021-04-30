---
UID: NF:comsvcs.ISecurityProperty.GetDirectCallerSID
title: ISecurityProperty::GetDirectCallerSID (comsvcs.h)
description: Retrieves the security identifier of the external process that called the currently executing method.
helpviewer_keywords: ["GetDirectCallerSID","GetDirectCallerSID method [COM+]","GetDirectCallerSID method [COM+]","ISecurityProperty interface","ISecurityProperty interface [COM+]","GetDirectCallerSID method","ISecurityProperty.GetDirectCallerSID","ISecurityProperty::GetDirectCallerSID","_cos_ISecurityProperty_GetDirectCallerSID","comsvcs/ISecurityProperty::GetDirectCallerSID","cos.isecurityproperty_getdirectcallersid"]
old-location: cos\isecurityproperty_getdirectcallersid.htm
tech.root: cos
ms.assetid: e322df62-25a4-40a3-9b80-da468a265162
ms.date: 12/05/2018
ms.keywords: GetDirectCallerSID, GetDirectCallerSID method [COM+], GetDirectCallerSID method [COM+],ISecurityProperty interface, ISecurityProperty interface [COM+],GetDirectCallerSID method, ISecurityProperty.GetDirectCallerSID, ISecurityProperty::GetDirectCallerSID, _cos_ISecurityProperty_GetDirectCallerSID, comsvcs/ISecurityProperty::GetDirectCallerSID, cos.isecurityproperty_getdirectcallersid
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
 - ISecurityProperty::GetDirectCallerSID
 - comsvcs/ISecurityProperty::GetDirectCallerSID
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
 - ISecurityProperty.GetDirectCallerSID
---

# ISecurityProperty::GetDirectCallerSID


## -description

Retrieves the security identifier of the external process that called the currently executing method.
 You can also obtain this information using <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>.

## -parameters

### -param pSID [out]

A reference to the security ID of the process from which the current method was invoked.

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
The security ID of the process that called the current method is returned in the parameter <i>pSid</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_NOCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The current object does not have a context associated with it because either the component was not imported into an application or the object was not created with one of the COM+ CreateInstance methods.

</td>
</tr>
</table>

## -remarks

Use the <b>GetDirectCallerSID</b> method to determine the security ID of the process that called the object's currently executing method. Security is enforced across process boundaries. This means that the security ID returned by <b>GetDirectCallerSID</b> is the security ID associated with the process that called into the process in which the current object is running, not necessarily the immediate caller into the object itself. If an object calls into another object within the same process, when the second object calls <b>GetDirectCallerSID</b> it gets the security ID of the most immediate caller outside its own process boundary, not the security ID of the object that directly called into it.

The following scenarios illustrate the functionality of the <b>GetDirectCallerSID</b> method:

<ul>
<li>A base process running on Server A, as user A, calls into Object X on Server B, running as user B. Then Object X calls into Object Y, running on Server C. If Object Y calls <b>GetDirectCallerSID</b>, the security ID of user B is returned.
</li>
<li>A base process, running on Server A as user A, calls into Object X on Server B, running as user B. Then Object X calls into Object Y, running in the same process as Object X, also on Server B. When Object Y calls <b>GetDirectCallerSID</b>, the security ID of user A is returned, not the security ID of user B.
</li>
</ul>
You must call <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-releasesid">ISecurityProperty::ReleaseSID</a> on a security ID when you finish using it.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityproperty">ISecurityProperty</a>