---
UID: NF:vsbackup.IVssBackupComponents.GatherWriterStatus
title: IVssBackupComponents::GatherWriterStatus (vsbackup.h)
description: The GatherWriterStatus method prompts each writer to send a status message.
helpviewer_keywords: ["GatherWriterStatus","GatherWriterStatus method [VSS]","GatherWriterStatus method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","GatherWriterStatus method","IVssBackupComponents.GatherWriterStatus","IVssBackupComponents::GatherWriterStatus","_win32_ivssbackupcomponents_gatherwriterstatus","base.ivssbackupcomponents_gatherwriterstatus","vsbackup/IVssBackupComponents::GatherWriterStatus"]
old-location: base\ivssbackupcomponents_gatherwriterstatus.htm
tech.root: base
ms.assetid: ca87cdc3-e233-4efc-81c0-918e5a698af5
ms.date: 12/05/2018
ms.keywords: GatherWriterStatus, GatherWriterStatus method [VSS], GatherWriterStatus method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GatherWriterStatus method, IVssBackupComponents.GatherWriterStatus, IVssBackupComponents::GatherWriterStatus, _win32_ivssbackupcomponents_gatherwriterstatus, base.ivssbackupcomponents_gatherwriterstatus, vsbackup/IVssBackupComponents::GatherWriterStatus
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
 - IVssBackupComponents::GatherWriterStatus
 - vsbackup/IVssBackupComponents::GatherWriterStatus
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
 - IVssBackupComponents.GatherWriterStatus
---

# IVssBackupComponents::GatherWriterStatus


## -description

The 
<b>GatherWriterStatus</b> method prompts each writer to send a status message.

## -parameters

### -param pAsync [out]

Doubly indirect pointer to an 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object containing the writer status data.

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
<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a> for the valid values returned by the <i>pHrResult</i> parameter.

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
<dt><b>VSS_E_WRITER_INFRASTRUCTURE</b></dt>
</dl>
</td>
<td width="60%">
The writer infrastructure is not operating properly. Check that the Event Service and VSS have been started, and check for errors associated with those services in the error log.

</td>
</tr>
</table>

## -remarks

The caller of this method should also call 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-freewriterstatus">IVssBackupComponents::FreeWriterStatus</a> after receiving the status of each writer.

After calling <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a>, requesters must call <b>GatherWriterStatus</b> to cause the writer session to be set to a completed state.

<div class="alert"><b>Note</b>  This is only necessary on Windows Server 2008 with Service Pack 2 (SP2) and earlier.</div>
<div> </div>
The 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> class handles the status message sent by each writer.

The caller is responsible for releasing the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-freewriterstatus">IVssBackupComponents::FreeWriterStatus</a>