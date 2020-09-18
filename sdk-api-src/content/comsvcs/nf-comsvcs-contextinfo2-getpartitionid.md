---
UID: NF:comsvcs.ContextInfo2.GetPartitionId
title: ContextInfo2::GetPartitionId (comsvcs.h)
description: Retrieves the GUID of the COM+ partition of the current object context.
helpviewer_keywords: ["ContextInfo2 interface [COM+]","GetPartitionId method","ContextInfo2.GetPartitionId","ContextInfo2::GetPartitionId","GetPartitionId","GetPartitionId method [COM+]","GetPartitionId method [COM+]","ContextInfo2 interface","_cos_ContextInfo2_GetPartitionId","comsvcs/ContextInfo2::GetPartitionId","cos.contextinfo2_getpartitionid"]
old-location: cos\contextinfo2_getpartitionid.htm
tech.root: cos
ms.assetid: b4cda75d-a4f3-404e-965a-9c1487946ee1
ms.date: 12/05/2018
ms.keywords: ContextInfo2 interface [COM+],GetPartitionId method, ContextInfo2.GetPartitionId, ContextInfo2::GetPartitionId, GetPartitionId, GetPartitionId method [COM+], GetPartitionId method [COM+],ContextInfo2 interface, _cos_ContextInfo2_GetPartitionId, comsvcs/ContextInfo2::GetPartitionId, cos.contextinfo2_getpartitionid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ContextInfo2::GetPartitionId
 - comsvcs/ContextInfo2::GetPartitionId
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
 - ContextInfo2.GetPartitionId
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

<a href="/windows/desktop/cossdk/com--partitions">COM+ Partitions</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo2">ContextInfo2</a>