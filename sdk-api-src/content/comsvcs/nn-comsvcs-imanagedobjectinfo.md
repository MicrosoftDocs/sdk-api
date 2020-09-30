---
UID: NN:comsvcs.IManagedObjectInfo
title: IManagedObjectInfo (comsvcs.h)
description: Describes the stub for a managed object.
helpviewer_keywords: ["IManagedObjectInfo","IManagedObjectInfo interface [COM+]","IManagedObjectInfo interface [COM+]","described","_cos_IManagedObjectInfo","comsvcs/IManagedObjectInfo","cos.imanagedobjectinfo"]
old-location: cos\imanagedobjectinfo.htm
tech.root: cos
ms.assetid: 7fa5f76e-df07-41b3-8fb0-62b84a034aa5
ms.date: 12/05/2018
ms.keywords: IManagedObjectInfo, IManagedObjectInfo interface [COM+], IManagedObjectInfo interface [COM+],described, _cos_IManagedObjectInfo, comsvcs/IManagedObjectInfo, cos.imanagedobjectinfo
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IManagedObjectInfo
 - comsvcs/IManagedObjectInfo
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
 - IManagedObjectInfo
---

# IManagedObjectInfo interface


## -description

Describes the stub for a managed object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManagedObjectInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IManagedObjectInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IManagedObjectInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-imanagedobjectinfo-getiobjectcontrol">GetIObjectControl</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a> interface that is associated with the managed object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-imanagedobjectinfo-getiunknown">GetIUnknown</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface that is associated with the managed object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-imanagedobjectinfo-setinpool">SetInPool</a>
</td>
<td align="left" width="63%">
Sets whether the managed object belongs to the COM+ object pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-imanagedobjectinfo-setwrapperstrength">SetWrapperStrength</a>
</td>
<td align="left" width="63%">
Sets whether the managed object holds a strong or a weak reference to the COM+ context.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nf-comsvcs-getmanagedextensions">GetManagedExtensions</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedactivationevents">IManagedActivationEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpoolaction">IManagedPoolAction</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpooledobj">IManagedPooledObj</a>