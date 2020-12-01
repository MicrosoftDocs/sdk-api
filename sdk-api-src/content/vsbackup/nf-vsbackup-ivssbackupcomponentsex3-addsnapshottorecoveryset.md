---
UID: NF:vsbackup.IVssBackupComponentsEx3.AddSnapshotToRecoverySet
title: IVssBackupComponentsEx3::AddSnapshotToRecoverySet (vsbackup.h)
description: Specifies the volumes to be included in a LUN resynchronization operation.
helpviewer_keywords: ["AddSnapshotToRecoverySet","AddSnapshotToRecoverySet method","AddSnapshotToRecoverySet method","IVssBackupComponentsEx3 interface","IVssBackupComponentsEx3 interface","AddSnapshotToRecoverySet method","IVssBackupComponentsEx3.AddSnapshotToRecoverySet","IVssBackupComponentsEx3::AddSnapshotToRecoverySet","base.ivssbackupcomponentsex3_addsnapshottorecoveryset","vsbackup/IVssBackupComponentsEx3::AddSnapshotToRecoverySet"]
old-location: base\ivssbackupcomponentsex3_addsnapshottorecoveryset.htm
tech.root: base
ms.assetid: f489d353-7c8a-45d2-8917-82d29fbdf5f5
ms.date: 12/05/2018
ms.keywords: AddSnapshotToRecoverySet, AddSnapshotToRecoverySet method, AddSnapshotToRecoverySet method,IVssBackupComponentsEx3 interface, IVssBackupComponentsEx3 interface,AddSnapshotToRecoverySet method, IVssBackupComponentsEx3.AddSnapshotToRecoverySet, IVssBackupComponentsEx3::AddSnapshotToRecoverySet, base.ivssbackupcomponentsex3_addsnapshottorecoveryset, vsbackup/IVssBackupComponentsEx3::AddSnapshotToRecoverySet
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - IVssBackupComponentsEx3::AddSnapshotToRecoverySet
 - vsbackup/IVssBackupComponentsEx3::AddSnapshotToRecoverySet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssBackupComponentsEx3.AddSnapshotToRecoverySet
---

# IVssBackupComponentsEx3::AddSnapshotToRecoverySet


## -description

Specifies the volumes to be included in a LUN resynchronization operation. This method is supported only on Windows server operating systems.

## -parameters

### -param snapshotId [in]

The identifier of the shadow copy that was returned by the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a> method during backup. This parameter is required and cannot be GUID_NULL.

### -param dwFlags [in]

This parameter is reserved and must be zero.

### -param pwszDestinationVolume [in, optional]

This parameter is optional and can be <b>NULL</b>. A value of <b>NULL</b> means that the contents of the shadow copy volume are to be copied back to the original volume. VSS identifies the original volume by the VDS_LUN_INFO information in the Backup Components Document.

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
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
<dt>0x80042301L</dt>
</dl>
</td>
<td width="60%">
Either there is no hardware provider that supports the operation, or the requester did not successfully add any volumes to the recovery set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_LEGACY_PROVIDER</b></dt>
<dt>0x800423F7L</dt>
</dl>
</td>
<td width="60%">
This version of the hardware provider does not support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The <i>snapshotId</i> parameter specifies a shadow copy that the hardware provider does not own.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_RESYNC_IN_PROGRESS</b></dt>
<dt>0x800423FFL</dt>
</dl>
</td>
<td width="60%">
Another LUN resynchronization operation is already in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_SNAPSHOT_NOT_IN_SET</b></dt>
<dt>0x8004232BL</dt>
</dl>
</td>
<td width="60%">
The <i>snapshotId</i> parameter specifies a shadow copy that does not exist in the Backup Components Document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED</b></dt>
<dt>0x8004230CL</dt>
</dl>
</td>
<td width="60%">
LUN resynchronization is not supported on this volume, because it is a dynamic volume, because the destination disk does not have a unique page 83 storage identifier, because the specified volume does not reside on a LUN managed by a VSS hardware provider, or because the destination disk is a cluster quorum disk. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex3">IVssBackupComponentsEx3</a>