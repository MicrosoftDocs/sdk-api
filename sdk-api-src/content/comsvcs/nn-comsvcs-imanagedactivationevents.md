---
UID: NN:comsvcs.IManagedActivationEvents
title: IManagedActivationEvents (comsvcs.h)
description: Used to create and destroy stubs for managed objects within the current COM+ context.
old-location: cos\imanagedactivationevents.htm
tech.root: cossdk
ms.assetid: 621ffc7d-186e-451c-8d97-9c8291549f51
ms.date: 12/05/2018
ms.keywords: IManagedActivationEvents, IManagedActivationEvents interface [COM+], IManagedActivationEvents interface [COM+],described, _cos_IManagedActivationEvents, comsvcs/IManagedActivationEvents, cos.imanagedactivationevents
ms.topic: interface
f1_keywords:
- comsvcs/IManagedActivationEvents
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IManagedActivationEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IManagedActivationEvents interface


## -description


Used to create and destroy stubs for managed objects within the current COM+ context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManagedActivationEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IManagedActivationEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IManagedActivationEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imanagedactivationevents-createmanagedstub">CreateManagedStub</a>
</td>
<td align="left" width="63%">
Creates a stub for a managed object within the current COM+ context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imanagedactivationevents-destroymanagedstub">DestroyManagedStub</a>
</td>
<td align="left" width="63%">
Destroys a stub that was created by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imanagedactivationevents-createmanagedstub">CreateManagedStub</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-getmanagedextensions">GetManagedExtensions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-imanagedobjectinfo">IManagedObjectInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpoolaction">IManagedPoolAction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpooledobj">IManagedPooledObj</a>
 

 

