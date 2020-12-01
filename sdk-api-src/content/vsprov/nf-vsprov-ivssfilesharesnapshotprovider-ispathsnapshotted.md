---
UID: NF:vsprov.IVssFileShareSnapshotProvider.IsPathSnapshotted
title: IVssFileShareSnapshotProvider::IsPathSnapshotted (vsprov.h)
description: Determines whether the given Universal Naming Convention (UNC) path currently has any snapshots.
helpviewer_keywords: ["IVssFileShareSnapshotProvider interface [VSS]","IsPathSnapshotted method","IVssFileShareSnapshotProvider.IsPathSnapshotted","IVssFileShareSnapshotProvider::IsPathSnapshotted","IsPathSnapshotted","IsPathSnapshotted method [VSS]","IsPathSnapshotted method [VSS]","IVssFileShareSnapshotProvider interface","base.ivssfilesharesnapshotprovider_ispathsnapshotted","vsprov/IVssFileShareSnapshotProvider::IsPathSnapshotted"]
old-location: base\ivssfilesharesnapshotprovider_ispathsnapshotted.htm
tech.root: base
ms.assetid: 9a885d5d-a441-4567-b562-39820fa7ffc1
ms.date: 12/05/2018
ms.keywords: IVssFileShareSnapshotProvider interface [VSS],IsPathSnapshotted method, IVssFileShareSnapshotProvider.IsPathSnapshotted, IVssFileShareSnapshotProvider::IsPathSnapshotted, IsPathSnapshotted, IsPathSnapshotted method [VSS], IsPathSnapshotted method [VSS],IVssFileShareSnapshotProvider interface, base.ivssfilesharesnapshotprovider_ispathsnapshotted, vsprov/IVssFileShareSnapshotProvider::IsPathSnapshotted
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
 - IVssFileShareSnapshotProvider::IsPathSnapshotted
 - vsprov/IVssFileShareSnapshotProvider::IsPathSnapshotted
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
 - IVssFileShareSnapshotProvider.IsPathSnapshotted
---

# IVssFileShareSnapshotProvider::IsPathSnapshotted


## -description

Determines whether the given Universal Naming Convention (UNC) path currently has any snapshots.

## -parameters

### -param pwszSharePath [in]

The path to the file share.

### -param pbSnapshotsPresent [out]

This parameter receives <b>TRUE</b> if the volume has a shadow copy, or <b>FALSE</b> if the volume does not have a shadow copy.

### -param plSnapshotCompatibility [out]

A bitmask of <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_compatibility">VSS_SNAPSHOT_COMPATIBILITY</a> values that indicate whether certain volume control or file I/O operations are disabled for the given volume, if the volume has a shadow copy.

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
The requested information was successfully returned.

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
The specified volume was not found.

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
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssfilesharesnapshotprovider">IVssFileShareSnapshotProvider</a>