---
UID: NF:winsync.ISyncChange.GetChangeVersion
title: ISyncChange::GetChangeVersion (winsync.h)
description: Gets the version that is associated with this change.
helpviewer_keywords: ["GetChangeVersion","GetChangeVersion method [Windows Sync]","GetChangeVersion method [Windows Sync]","ISyncChange interface","ISyncChange interface [Windows Sync]","GetChangeVersion method","ISyncChange.GetChangeVersion","ISyncChange::GetChangeVersion","winsync.isyncchange_getchangeversion","winsync/ISyncChange::GetChangeVersion"]
old-location: winsync\isyncchange_getchangeversion.htm
tech.root: winsync
ms.assetid: 6b6def94-8c48-41f6-8869-e28d0db0d500
ms.date: 12/05/2018
ms.keywords: GetChangeVersion, GetChangeVersion method [Windows Sync], GetChangeVersion method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetChangeVersion method, ISyncChange.GetChangeVersion, ISyncChange::GetChangeVersion, winsync.isyncchange_getchangeversion, winsync/ISyncChange::GetChangeVersion
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
 - ISyncChange::GetChangeVersion
 - winsync/ISyncChange::GetChangeVersion
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
 - ISyncChange.GetChangeVersion
---

# ISyncChange::GetChangeVersion


## -description

Gets the version that is associated with this change.

## -parameters

### -param pbCurrentReplicaId [in]

The ID of the replica that owns this change. The ID format must match the format that is specified by the <a href="/windows/desktop/api/winsync/ns-winsync-id_parameters">ID_PARAMETERS</a> property of the provider.

### -param pVersion [out]

Returns the change version of the item.

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
<dt><b>SYNC_E_ITEM_HAS_NO_VERSION_DATA</b></dt>
</dl>
</td>
<td width="60%">
The item has been forgotten.

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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ITEM_HAS_CHANGE_UNITS</b></dt>
</dl>
</td>
<td width="60%">
The item has change units.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_version">SYNC VERSION Structure</a>