---
UID: NF:comsvcs.ISecurityProperty.ReleaseSID
title: ISecurityProperty::ReleaseSID (comsvcs.h)
description: Releases the security identifier returned by one of the other ISecurityProperty methods.
helpviewer_keywords: ["ISecurityProperty interface [COM+]","ReleaseSID method","ISecurityProperty.ReleaseSID","ISecurityProperty::ReleaseSID","ReleaseSID","ReleaseSID method [COM+]","ReleaseSID method [COM+]","ISecurityProperty interface","_cos_ISecurityProperty_ReleaseSID","comsvcs/ISecurityProperty::ReleaseSID","cos.isecurityproperty_releasesid"]
old-location: cos\isecurityproperty_releasesid.htm
tech.root: cos
ms.assetid: 572bf3fd-eb85-40de-b607-26b77b9d9cf8
ms.date: 12/05/2018
ms.keywords: ISecurityProperty interface [COM+],ReleaseSID method, ISecurityProperty.ReleaseSID, ISecurityProperty::ReleaseSID, ReleaseSID, ReleaseSID method [COM+], ReleaseSID method [COM+],ISecurityProperty interface, _cos_ISecurityProperty_ReleaseSID, comsvcs/ISecurityProperty::ReleaseSID, cos.isecurityproperty_releasesid
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
 - ISecurityProperty::ReleaseSID
 - comsvcs/ISecurityProperty::ReleaseSID
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
 - ISecurityProperty.ReleaseSID
---

# ISecurityProperty::ReleaseSID


## -description

Releases the security identifier returned by one of the other <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityproperty">ISecurityProperty</a> methods.

## -parameters

### -param pSID [in]

A reference to a security ID.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument passed in the pSid parameter is not a reference to a security ID.

</td>
</tr>
</table>

## -remarks

You should always invoke the <b>ReleaseSID</b> method to release any security ID pointers returned by the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-getdirectcallersid">GetDirectCallerSID</a>, <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-getdirectcreatorsid">GetDirectCreatorSID</a>, <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-getoriginalcallersid">GetOriginalCallerSID</a>, and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-getoriginalcreatorsid">GetOriginalCreatorSID</a> methods.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityproperty">ISecurityProperty</a>