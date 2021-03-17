---
UID: NF:winsync.ISyncChange.GetCreationVersion
title: ISyncChange::GetCreationVersion (winsync.h)
description: Gets the creation version of the changed item.
helpviewer_keywords: ["GetCreationVersion","GetCreationVersion method [Windows Sync]","GetCreationVersion method [Windows Sync]","ISyncChange interface","ISyncChange interface [Windows Sync]","GetCreationVersion method","ISyncChange.GetCreationVersion","ISyncChange::GetCreationVersion","winsync.isyncchange_getcreationversion","winsync/ISyncChange::GetCreationVersion"]
old-location: winsync\isyncchange_getcreationversion.htm
tech.root: winsync
ms.assetid: 2c795cbe-b587-42ef-9200-b7d0d972e7c7
ms.date: 12/05/2018
ms.keywords: GetCreationVersion, GetCreationVersion method [Windows Sync], GetCreationVersion method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetCreationVersion method, ISyncChange.GetCreationVersion, ISyncChange::GetCreationVersion, winsync.isyncchange_getcreationversion, winsync/ISyncChange::GetCreationVersion
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - ISyncChange::GetCreationVersion
 - winsync/ISyncChange::GetCreationVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChange.GetCreationVersion
---

# ISyncChange::GetCreationVersion


## -description

Gets the creation version of the changed item.

## -parameters

### -param pbCurrentReplicaId [in]

The ID of the replica that owns this change. The ID format must match the format that is specified by the <a href="/windows/desktop/api/winsync/ns-winsync-id_parameters">ID_PARAMETERS</a> property of the provider.

### -param pVersion [out]

Returns the creation version of the item.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i> pbCurrentReplicaId</i> is not the correct replica ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
<i> pbCurrentReplicaId</i> is not in the format that is specified by the ID format schema of the provider.


</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_version">SYNC VERSION Structure</a>