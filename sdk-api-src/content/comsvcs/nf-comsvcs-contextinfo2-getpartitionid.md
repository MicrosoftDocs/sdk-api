---
UID: NF:comsvcs.ContextInfo2.GetPartitionId
title: ContextInfo2::GetPartitionId (comsvcs.h)
author: windows-sdk-content
description: Retrieves the GUID of the COM+ partition of the current object context.
old-location: cos\contextinfo2_getpartitionid.htm
tech.root: cossdk
ms.assetid: b4cda75d-a4f3-404e-965a-9c1487946ee1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ContextInfo2 interface [COM+],GetPartitionId method, ContextInfo2.GetPartitionId, ContextInfo2::GetPartitionId, GetPartitionId, GetPartitionId method [COM+], GetPartitionId method [COM+],ContextInfo2 interface, _cos_ContextInfo2_GetPartitionId, comsvcs/ContextInfo2::GetPartitionId, cos.contextinfo2_getpartitionid
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - ContextInfo2.GetPartitionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ContextInfo2::GetPartitionId


## -description


Retrieves the GUID of the COM+ partition of the current object context.


## -parameters




### -param __MIDL__ContextInfo20000 [out]

A reference to the partition identifier.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_PARTITIONS_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
COM+ partitions are not enabled.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fd22a64c-f2d8-48af-86e1-985e21b0f8fa">COM+ Partitions</a>



<a href="https://msdn.microsoft.com/06954cc5-19a7-4bae-ac30-94dcdc35d15d">ContextInfo2</a>
 

 

