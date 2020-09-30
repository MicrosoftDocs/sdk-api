---
UID: NF:vsbackup.IVssBackupComponents.StartSnapshotSet
title: IVssBackupComponents::StartSnapshotSet (vsbackup.h)
description: The StartSnapshotSet method creates a new, empty shadow copy set.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","StartSnapshotSet method","IVssBackupComponents.StartSnapshotSet","IVssBackupComponents::StartSnapshotSet","StartSnapshotSet","StartSnapshotSet method [VSS]","StartSnapshotSet method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_startsnapshotset","base.ivssbackupcomponents_startsnapshotset","vsbackup/IVssBackupComponents::StartSnapshotSet"]
old-location: base\ivssbackupcomponents_startsnapshotset.htm
tech.root: base
ms.assetid: 6a0a6228-2131-48a6-8d18-9491969d265b
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],StartSnapshotSet method, IVssBackupComponents.StartSnapshotSet, IVssBackupComponents::StartSnapshotSet, StartSnapshotSet, StartSnapshotSet method [VSS], StartSnapshotSet method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_startsnapshotset, base.ivssbackupcomponents_startsnapshotset, vsbackup/IVssBackupComponents::StartSnapshotSet
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponents::StartSnapshotSet
 - vsbackup/IVssBackupComponents::StartSnapshotSet
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
 - IVssBackupComponents.StartSnapshotSet
---

# IVssBackupComponents::StartSnapshotSet


## -description

The 
<b>StartSnapshotSet</b> method creates a new, empty shadow copy set.

## -parameters

### -param pSnapshotSetId [out]

The address of a caller-allocated variable that receives the shadow copy set identifier.

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
Successfully started the shadow copy set.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_SNAPSHOT_SET_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The creation of a shadow copy is in progress, and only one shadow copy creation operation can be in progress at one time. Either wait to try again or return with a failure error code.

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

## -remarks

This method must be called before 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a> during backup operations.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>