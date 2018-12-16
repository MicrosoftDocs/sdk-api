---
UID: NN:comsvcs.IManagedObjectInfo
title: IManagedObjectInfo
author: windows-sdk-content
description: Describes the stub for a managed object.
old-location: cos\imanagedobjectinfo.htm
tech.root: cossdk
ms.assetid: 7fa5f76e-df07-41b3-8fb0-62b84a034aa5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IManagedObjectInfo, IManagedObjectInfo interface [COM+], IManagedObjectInfo interface [COM+],described, _cos_IManagedObjectInfo, comsvcs/IManagedObjectInfo, cos.imanagedobjectinfo
ms.topic: interface
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
 - IManagedObjectInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManagedObjectInfo interface


## -description


Describes the stub for a managed object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManagedObjectInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IManagedObjectInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0ce1408a-488e-4705-8155-445e1be8c51f">GetIObjectControl</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/cbc63f97-dfc7-4e1f-97f9-2043f8bea1d4">IObjectControl</a> interface that is associated with the managed object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c0d27cb-1725-4654-ab15-0ef815ce6657">GetIUnknown</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface that is associated with the managed object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fef3842f-acf7-4aff-801d-17343633be8c">SetInPool</a>
</td>
<td align="left" width="63%">
Sets whether the managed object belongs to the COM+ object pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f03c6cb-4bfc-4871-8f5b-78ccc8df8838">SetWrapperStrength</a>
</td>
<td align="left" width="63%">
Sets whether the managed object holds a strong or a weak reference to the COM+ context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cffd18c4-6e37-447b-b749-64793711ea56">GetManagedExtensions</a>



<a href="https://msdn.microsoft.com/621ffc7d-186e-451c-8d97-9c8291549f51">IManagedActivationEvents</a>



<a href="https://msdn.microsoft.com/6c29bbe0-840f-4eaf-97ad-40b0f89cadfd">IManagedPoolAction</a>



<a href="https://msdn.microsoft.com/04853859-5d85-4b88-9e1b-422e3454fd3f">IManagedPooledObj</a>
 

 

