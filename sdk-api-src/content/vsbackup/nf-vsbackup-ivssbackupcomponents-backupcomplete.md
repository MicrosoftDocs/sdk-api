---
UID: NF:vsbackup.IVssBackupComponents.BackupComplete
title: IVssBackupComponents::BackupComplete (vsbackup.h)
description: The BackupComplete method causes VSS to generate a BackupComplete event, which signals writers that the backup process has completed.
helpviewer_keywords: ["BackupComplete","BackupComplete method [VSS]","BackupComplete method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","BackupComplete method","IVssBackupComponents.BackupComplete","IVssBackupComponents::BackupComplete","_win32_ivssbackupcomponents_backupcomplete","base.ivssbackupcomponents_backupcomplete","vsbackup/IVssBackupComponents::BackupComplete"]
old-location: base\ivssbackupcomponents_backupcomplete.htm
tech.root: base
ms.assetid: ee49d4b1-f3f4-4c85-a3a2-f4452d066f21
ms.date: 12/05/2018
ms.keywords: BackupComplete, BackupComplete method [VSS], BackupComplete method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],BackupComplete method, IVssBackupComponents.BackupComplete, IVssBackupComponents::BackupComplete, _win32_ivssbackupcomponents_backupcomplete, base.ivssbackupcomponents_backupcomplete, vsbackup/IVssBackupComponents::BackupComplete
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
 - IVssBackupComponents::BackupComplete
 - vsbackup/IVssBackupComponents::BackupComplete
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
 - IVssBackupComponents.BackupComplete
---

# IVssBackupComponents::BackupComplete


## -description

The 
    <b>BackupComplete</b> method causes VSS to generate a 
    <b>BackupComplete</b> event, which signals writers 
    that the backup process has completed.

## -parameters

### -param ppAsync [out]

Doubly indirect pointer to an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> instance.

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
Successfully returned a pointer to an instance of the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface. Refer to <a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a> for the valid values returned by the <i>pHrResult</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAsync</i> does not point to a valid pointer; that is, it is <b>NULL</b>.

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
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED_WRITER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred during communication with writers. The error code is logged in the error log file. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>

## -remarks

When working in component mode (<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a> was called with a select components argument of <b>TRUE</b>), writers can determine the success or failure of the backup of any component explicitly included in the Backup Components Document components by using 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupsucceeded">IVssComponent::GetBackupSucceeded</a>. Therefore, a well-behaved backup application (requester) must call 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded">IVssBackupComponents::SetBackupSucceeded</a> after each component has been processed and prior to calling 
<b>BackupComplete</b>.

Do not call this method if the call to <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a> failed. For more information about how requesters use  <b>DoSnapshotSet</b>, <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded">SetBackupSucceeded</a>, and <b>BackupComplete</b> in a backup operation, see <a href="/windows/desktop/VSS/overview-of-pre-backup-tasks">Overview of Pre-Backup Tasks</a> and <a href="/windows/desktop/VSS/overview-of-actual-backup-of-files">Overview of Actual Backup Of Files</a>.

This operation is asynchronous. The caller can use the 
<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">QueryStatus</a> interface method in the returned 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface to determine the status of the notification.

After calling <b>BackupComplete</b>, requesters must call <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">GatherWriterStatus</a> to cause the writer session to be set to a completed state.

<div class="alert"><b>Note</b>  This is only necessary on Windows Server 2008 with Service Pack 2 (SP2) and earlier.</div>
<div> </div>
The backup application can choose to abort the backup at any time after the shadow copy is created by calling 
<a href="/windows/desktop/api/vss/nf-vss-ivssasync-cancel">IVssAsync::Cancel</a>.

The calling application is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the resources held by the returned 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> when it is no longer needed.

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vss/nf-vss-ivssasync-cancel">IVssAsync::Cancel</a>



<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded">IVssBackupComponents::SetBackupSucceeded</a>