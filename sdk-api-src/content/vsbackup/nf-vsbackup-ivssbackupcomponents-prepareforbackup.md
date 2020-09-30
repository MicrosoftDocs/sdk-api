---
UID: NF:vsbackup.IVssBackupComponents.PrepareForBackup
title: IVssBackupComponents::PrepareForBackup (vsbackup.h)
description: The PrepareForBackup method will cause VSS to generate a PrepareForBackup event, signaling writers to prepare for an upcoming backup operation. This makes a requester's Backup Components Document available to writers.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","PrepareForBackup method","IVssBackupComponents.PrepareForBackup","IVssBackupComponents::PrepareForBackup","PrepareForBackup","PrepareForBackup method [VSS]","PrepareForBackup method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_prepareforbackup","base.ivssbackupcomponents_prepareforbackup","vsbackup/IVssBackupComponents::PrepareForBackup"]
old-location: base\ivssbackupcomponents_prepareforbackup.htm
tech.root: base
ms.assetid: 46ce8282-a434-4b0b-b66e-40810052b34b
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],PrepareForBackup method, IVssBackupComponents.PrepareForBackup, IVssBackupComponents::PrepareForBackup, PrepareForBackup, PrepareForBackup method [VSS], PrepareForBackup method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_prepareforbackup, base.ivssbackupcomponents_prepareforbackup, vsbackup/IVssBackupComponents::PrepareForBackup
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
 - IVssBackupComponents::PrepareForBackup
 - vsbackup/IVssBackupComponents::PrepareForBackup
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
 - IVssBackupComponents.PrepareForBackup
---

# IVssBackupComponents::PrepareForBackup


## -description

The 
<b>PrepareForBackup</b> method will cause VSS to generate a 
<a href="/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> event, signaling writers to prepare for an upcoming backup operation. This makes a requester's Backup Components Document available to writers.

## -parameters

### -param ppAsync [out]

Doubly indirect pointer to an instance of the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface that is used to determine when the asynchronous operation is complete.

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
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface. See 
<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a> for the error codes returned in the <i>pHrResult</i> parameter.

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
</table>

## -remarks

<b>PrepareForBackup</b> generates a 
PrepareForBackup event, which is handled by each instance of each writer through the 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a> method.

Before 
<b>PrepareForBackup</b> can be called, 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a> must be called.

The Backup Components Document can still be modified by writers in their 
<b>PrepareForBackup</b> event handler (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>), and afterward until the generation of a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event.

The caller is responsible for releasing the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface.

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset">IVssBackupComponents::StartSnapshotSet</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>