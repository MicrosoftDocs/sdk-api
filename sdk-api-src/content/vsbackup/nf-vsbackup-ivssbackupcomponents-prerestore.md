---
UID: NF:vsbackup.IVssBackupComponents.PreRestore
title: IVssBackupComponents::PreRestore (vsbackup.h)
description: The PreRestore method will cause VSS to generate a PreRestore event, signaling writers to prepare for an upcoming restore operation.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","PreRestore method","IVssBackupComponents.PreRestore","IVssBackupComponents::PreRestore","PreRestore","PreRestore method [VSS]","PreRestore method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_prerestore","base.ivssbackupcomponents_prerestore","vsbackup/IVssBackupComponents::PreRestore"]
old-location: base\ivssbackupcomponents_prerestore.htm
tech.root: base
ms.assetid: 7a4c8869-9655-49a7-818b-98a08103f4b4
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],PreRestore method, IVssBackupComponents.PreRestore, IVssBackupComponents::PreRestore, PreRestore, PreRestore method [VSS], PreRestore method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_prerestore, base.ivssbackupcomponents_prerestore, vsbackup/IVssBackupComponents::PreRestore
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
 - IVssBackupComponents::PreRestore
 - vsbackup/IVssBackupComponents::PreRestore
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
 - IVssBackupComponents.PreRestore
---

# IVssBackupComponents::PreRestore


## -description

The 
<b>PreRestore</b> method will cause VSS to generate a 
<a href="/windows/desktop/VSS/vssgloss-p">PreRestore</a> event, signaling writers to prepare for an upcoming restore operation.

## -parameters

### -param ppAsync [out]

Doubly indirect pointer to an 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object containing status data for the signaled event.

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
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface. Refer to <a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a> for the error codes returned in the <i>pHrResult</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppAsync</i> parameter does not point to a valid pointer; that is, it is <b>NULL</b>.

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

The caller is responsible for releasing the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer.

Special consideration should be given to EFI systems when the requester has selected the Automated System Recovery (ASR) writer for restore.  If you are restoring to a disk that contains the EFI partition, and one of the following conditions exists, you must first clean the disk by calling the <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-clean">IVdsAdvancedDisk::Clean</a> method:

<ul>
<li>You are restoring to an EFI system disk whose partitioning has changed since the last ASR backup.</li>
<li>You are restoring to a different physical drive than the one from which the backup was taken.</li>
</ul>
Failure to perform this disk-cleaning step may result in unexpected results during <a href="/windows/desktop/VSS/vssgloss-p">PreRestore</a>.

For more information about the ASR writer, see <a href="/windows/desktop/VSS/in-box-vss-writers">In-Box VSS Writers</a>.

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>