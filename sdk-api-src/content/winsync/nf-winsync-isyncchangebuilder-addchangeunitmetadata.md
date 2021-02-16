---
UID: NF:winsync.ISyncChangeBuilder.AddChangeUnitMetadata
title: ISyncChangeBuilder::AddChangeUnitMetadata (winsync.h)
description: Adds change unit metadata to an item change.
helpviewer_keywords: ["AddChangeUnitMetadata","AddChangeUnitMetadata method [Windows Sync]","AddChangeUnitMetadata method [Windows Sync]","ISyncChangeBuilder interface","ISyncChangeBuilder interface [Windows Sync]","AddChangeUnitMetadata method","ISyncChangeBuilder.AddChangeUnitMetadata","ISyncChangeBuilder::AddChangeUnitMetadata","winsync.isyncchangebuilder_addchangeunitmetadata","winsync/ISyncChangeBuilder::AddChangeUnitMetadata"]
old-location: winsync\isyncchangebuilder_addchangeunitmetadata.htm
tech.root: winsync
ms.assetid: 218e0f9d-9471-4b21-a424-b1298da2fb23
ms.date: 12/05/2018
ms.keywords: AddChangeUnitMetadata, AddChangeUnitMetadata method [Windows Sync], AddChangeUnitMetadata method [Windows Sync],ISyncChangeBuilder interface, ISyncChangeBuilder interface [Windows Sync],AddChangeUnitMetadata method, ISyncChangeBuilder.AddChangeUnitMetadata, ISyncChangeBuilder::AddChangeUnitMetadata, winsync.isyncchangebuilder_addchangeunitmetadata, winsync/ISyncChangeBuilder::AddChangeUnitMetadata
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
 - ISyncChangeBuilder::AddChangeUnitMetadata
 - winsync/ISyncChangeBuilder::AddChangeUnitMetadata
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
 - ISyncChangeBuilder.AddChangeUnitMetadata
---

# ISyncChangeBuilder::AddChangeUnitMetadata


## -description

Adds change unit metadata to an item change.

## -parameters

### -param pbChangeUnitId [in]

The ID of the change unit to add to the item change.

### -param pChangeUnitVersion [in]

The version of the change unit change to add to the item change.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The format of the change unit ID that is contained in <i>pbChangeUnitId</i> does not match the format that is specified by the ID format schema of the provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The item change to which to add this change unit to has <b>SYNC_CHANGE_FLAG_DELETE</b> or <b>SYNC_CHANGE_FLAG_DOES_NOT_EXIST</b> set as one of its flags.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebuilder">ISyncChangeBuilder Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_version">SYNC_VERSION Structure</a>