---
UID: NF:vsprov.IVssFileShareSnapshotProvider.DeleteSnapshots
title: IVssFileShareSnapshotProvider::DeleteSnapshots (vsprov.h)
description: Deletes specific snapshots, or all snapshots in a specified snapshot set.
helpviewer_keywords: ["DeleteSnapshots","DeleteSnapshots method [VSS]","DeleteSnapshots method [VSS]","IVssFileShareSnapshotProvider interface","IVssFileShareSnapshotProvider interface [VSS]","DeleteSnapshots method","IVssFileShareSnapshotProvider.DeleteSnapshots","IVssFileShareSnapshotProvider::DeleteSnapshots","base.ivssfilesharesnapshotprovider_deletesnapshots","vsprov/IVssFileShareSnapshotProvider::DeleteSnapshots"]
old-location: base\ivssfilesharesnapshotprovider_deletesnapshots.htm
tech.root: base
ms.assetid: 3fd48346-8a85-4ddf-9a6d-ac0cb82d4133
ms.date: 12/05/2018
ms.keywords: DeleteSnapshots, DeleteSnapshots method [VSS], DeleteSnapshots method [VSS],IVssFileShareSnapshotProvider interface, IVssFileShareSnapshotProvider interface [VSS],DeleteSnapshots method, IVssFileShareSnapshotProvider.DeleteSnapshots, IVssFileShareSnapshotProvider::DeleteSnapshots, base.ivssfilesharesnapshotprovider_deletesnapshots, vsprov/IVssFileShareSnapshotProvider::DeleteSnapshots
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssFileShareSnapshotProvider::DeleteSnapshots
 - vsprov/IVssFileShareSnapshotProvider::DeleteSnapshots
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssFileShareSnapshotProvider.DeleteSnapshots
---

# IVssFileShareSnapshotProvider::DeleteSnapshots


## -description

Deletes specific snapshots, or all snapshots in a specified snapshot set.

## -parameters

### -param SourceObjectId [in]

Identifier of the shadow copy or shadow copy set to be deleted.

### -param eSourceObjectType [in]

Type of the object to be deleted. The value of this parameter is VSS_OBJECT_SNAPSHOT or VSS_OBJECT_SNAPSHOT_SET.

### -param bForceDelete [in]

If the value of this parameter is <b>TRUE</b>, the provider will do everything possible to delete the shadow copy or shadow copies in a shadow copy set. If it is <b>FALSE</b>, no additional effort will be made.

### -param plDeletedSnapshots [out]

Pointer to a variable that receives the number of shadow copies that were deleted.

### -param pNondeletedSnapshotID [out]

If an error occurs, this parameter receives a pointer to the identifier of the first shadow copy that could not be deleted. Otherwise, it points to GUID_NULL.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The shadow copies were successfully deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified shadow copies were not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Provider error. The provider logged the error in the event log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>

## -remarks

The VSS coordinator calls this method as part of the snapshot auto-release process.  The method is also called in response to requester driven delete operations.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssfilesharesnapshotprovider">IVssFileShareSnapshotProvider</a>