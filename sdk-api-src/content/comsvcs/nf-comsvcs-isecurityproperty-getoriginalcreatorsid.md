---
UID: NF:comsvcs.ISecurityProperty.GetOriginalCreatorSID
title: ISecurityProperty::GetOriginalCreatorSID (comsvcs.h)
description: In MTS 2.0, this method retrieves the security identifier of the base process that initiated the activity in which the current object is executing. Do not use this method in COM+.
helpviewer_keywords: ["GetOriginalCreatorSID","GetOriginalCreatorSID method [COM+]","GetOriginalCreatorSID method [COM+]","ISecurityProperty interface","ISecurityProperty interface [COM+]","GetOriginalCreatorSID method","ISecurityProperty.GetOriginalCreatorSID","ISecurityProperty::GetOriginalCreatorSID","_cos_ISecurityProperty_GetOriginalCreatorSID","comsvcs/ISecurityProperty::GetOriginalCreatorSID","cos.isecurityproperty_getoriginalcreatorsid"]
old-location: cos\isecurityproperty_getoriginalcreatorsid.htm
tech.root: cos
ms.assetid: 599b0773-feee-4e3d-a23b-cc2c294f49f9
ms.date: 12/05/2018
ms.keywords: GetOriginalCreatorSID, GetOriginalCreatorSID method [COM+], GetOriginalCreatorSID method [COM+],ISecurityProperty interface, ISecurityProperty interface [COM+],GetOriginalCreatorSID method, ISecurityProperty.GetOriginalCreatorSID, ISecurityProperty::GetOriginalCreatorSID, _cos_ISecurityProperty_GetOriginalCreatorSID, comsvcs/ISecurityProperty::GetOriginalCreatorSID, cos.isecurityproperty_getoriginalcreatorsid
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
 - ISecurityProperty::GetOriginalCreatorSID
 - comsvcs/ISecurityProperty::GetOriginalCreatorSID
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
 - ISecurityProperty.GetOriginalCreatorSID
---

# ISecurityProperty::GetOriginalCreatorSID


## -description

In MTS 2.0, this method retrieves the security identifier of the base process that initiated the activity in which the current object is executing. Do not use this method in COM+.

## -parameters

### -param pSID [out]

A reference to the security ID of the base process that initiated the activity in which the current object is executing.

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
The security ID of the original created is returned in the parameter <i>pSid</i>.

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

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityproperty">ISecurityProperty</a>