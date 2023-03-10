---
UID: NF:vsbackup.IVssBackupComponents.AbortBackup
title: IVssBackupComponents::AbortBackup (vsbackup.h)
description: The AbortBackup method notifies VSS that a backup operation was terminated.
helpviewer_keywords: ["AbortBackup","AbortBackup method [VSS]","AbortBackup method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","AbortBackup method","IVssBackupComponents.AbortBackup","IVssBackupComponents::AbortBackup","_win32_ivssbackupcomponents_abortbackup","base.ivssbackupcomponents_abortbackup","vsbackup/IVssBackupComponents::AbortBackup"]
old-location: base\ivssbackupcomponents_abortbackup.htm
tech.root: base
ms.assetid: e854ab83-9a1a-4660-8a3e-37747b1b7d8c
ms.date: 12/05/2018
ms.keywords: AbortBackup, AbortBackup method [VSS], AbortBackup method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],AbortBackup method, IVssBackupComponents.AbortBackup, IVssBackupComponents::AbortBackup, _win32_ivssbackupcomponents_abortbackup, base.ivssbackupcomponents_abortbackup, vsbackup/IVssBackupComponents::AbortBackup
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
 - IVssBackupComponents::AbortBackup
 - vsbackup/IVssBackupComponents::AbortBackup
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
 - IVssBackupComponents.AbortBackup
---

# IVssBackupComponents::AbortBackup


## -description

The 
<b>AbortBackup</b> method notifies VSS that a backup operation was terminated.

This method must be called if a backup operation terminates after the creation of a shadow copy set with 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset">IVssBackupComponents::StartSnapshotSet</a> and before 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a> returns.

If 
<b>AbortBackup</b> is called and no shadow copy or backup operations are underway, it is ignored.



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
The query operation was successful.

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
The backup components object is not initialized.

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

<b>AbortBackup</b> generates an <a href="/windows/desktop/VSS/vssgloss-a">Abort</a> event, which is handled by each instance of each writer through the 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onabort">CVssWriter::OnAbort</a> method.

## -see-also

<a href="/windows/desktop/api/vss/nf-vss-ivssasync-cancel">IVssAsync::Cancel</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">IVssBackupComponents::BackupComplete</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset">IVssBackupComponents::StartSnapshotSet</a>
