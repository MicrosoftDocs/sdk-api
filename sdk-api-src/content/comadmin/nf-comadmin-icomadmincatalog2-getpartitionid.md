---
UID: NF:comadmin.ICOMAdminCatalog2.GetPartitionID
title: ICOMAdminCatalog2::GetPartitionID (comadmin.h)
description: Retrieves the partition identifier for the specified COM+ application.
helpviewer_keywords: ["GetPartitionID","GetPartitionID method [COM+]","GetPartitionID method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","GetPartitionID method","ICOMAdminCatalog2.GetPartitionID","ICOMAdminCatalog2::GetPartitionID","_cos_icomadmincatalog2_GetPartitionID","comadmin/ICOMAdminCatalog2::GetPartitionID","cos.icomadmincatalog2_getpartitionid"]
old-location: cos\icomadmincatalog2_getpartitionid.htm
tech.root: cos
ms.assetid: 12fa83e1-b2d2-48c3-a002-ac2f8043b54a
ms.date: 12/05/2018
ms.keywords: GetPartitionID, GetPartitionID method [COM+], GetPartitionID method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],GetPartitionID method, ICOMAdminCatalog2.GetPartitionID, ICOMAdminCatalog2::GetPartitionID, _cos_icomadmincatalog2_GetPartitionID, comadmin/ICOMAdminCatalog2::GetPartitionID, cos.icomadmincatalog2_getpartitionid
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ICOMAdminCatalog2::GetPartitionID
 - comadmin/ICOMAdminCatalog2::GetPartitionID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.GetPartitionID
---

# ICOMAdminCatalog2::GetPartitionID


## -description

Retrieves  the partition identifier for the specified COM+ application.

## -parameters

### -param bstrApplicationIDOrName [in]

The application ID or name of a COM+ application.

### -param pbstrPartitionID [out, retval]

The partition GUID associated with the specified application.

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
<dt><b>COMADMIN_E_AMBIGUOUS_APPLICATION_NAME</b></dt>
</dl>
</td>
<td width="60%">
The named application exists in multiple partitions. To avoid this error, use an application ID instead of a name.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>