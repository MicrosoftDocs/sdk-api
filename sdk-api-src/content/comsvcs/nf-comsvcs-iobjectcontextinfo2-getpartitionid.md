---
UID: NF:comsvcs.IObjectContextInfo2.GetPartitionId
title: IObjectContextInfo2::GetPartitionId (comsvcs.h)
description: Retrieves the identifier of the partition of the current object context.
helpviewer_keywords: ["GetPartitionId","GetPartitionId method [COM+]","GetPartitionId method [COM+]","IObjectContextInfo2 interface","IObjectContextInfo2 interface [COM+]","GetPartitionId method","IObjectContextInfo2.GetPartitionId","IObjectContextInfo2::GetPartitionId","_cos_IObjectContextInfo2_GetPartitionId","comsvcs/IObjectContextInfo2::GetPartitionId","cos.iobjectcontextinfo2_getpartitionid"]
old-location: cos\iobjectcontextinfo2_getpartitionid.htm
tech.root: cos
ms.assetid: 090afcec-d124-4b7c-822a-ecb56f9037a6
ms.date: 12/05/2018
ms.keywords: GetPartitionId, GetPartitionId method [COM+], GetPartitionId method [COM+],IObjectContextInfo2 interface, IObjectContextInfo2 interface [COM+],GetPartitionId method, IObjectContextInfo2.GetPartitionId, IObjectContextInfo2::GetPartitionId, _cos_IObjectContextInfo2_GetPartitionId, comsvcs/IObjectContextInfo2::GetPartitionId, cos.iobjectcontextinfo2_getpartitionid
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
 - IObjectContextInfo2::GetPartitionId
 - comsvcs/IObjectContextInfo2::GetPartitionId
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
 - IObjectContextInfo2.GetPartitionId
---

# IObjectContextInfo2::GetPartitionId


## -description

Retrieves the identifier of the partition of the current object context.

## -parameters

### -param pGuid [out]

A GUID that identifies the COM+ partition.

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
<dt><b>COMADMIN_E_PARTITIONS_DISABLED </b></dt>
</dl>
</td>
<td width="60%">
COM+ partitions are not enabled.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a>