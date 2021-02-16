---
UID: NF:vsbackup.IVssBackupComponents.SetRestoreState
title: IVssBackupComponents::SetRestoreState (vsbackup.h)
description: The SetRestoreState method defines an overall configuration for a restore operation.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetRestoreState method","IVssBackupComponents.SetRestoreState","IVssBackupComponents::SetRestoreState","SetRestoreState","SetRestoreState method [VSS]","SetRestoreState method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setrestorestate","base.ivssbackupcomponents_setrestorestate","vsbackup/IVssBackupComponents::SetRestoreState"]
old-location: base\ivssbackupcomponents_setrestorestate.htm
tech.root: base
ms.assetid: bc85e93f-1034-41cc-bf69-025aa86a56fd
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetRestoreState method, IVssBackupComponents.SetRestoreState, IVssBackupComponents::SetRestoreState, SetRestoreState, SetRestoreState method [VSS], SetRestoreState method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setrestorestate, base.ivssbackupcomponents_setrestorestate, vsbackup/IVssBackupComponents::SetRestoreState
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IVssBackupComponents::SetRestoreState
 - vsbackup/IVssBackupComponents::SetRestoreState
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
 - IVssBackupComponents.SetRestoreState
---

# IVssBackupComponents::SetRestoreState


## -description

The 
<b>SetRestoreState</b> method defines an overall configuration for a restore operation.

## -parameters

### -param restoreType [in]

A 
<a href="/windows/desktop/api/vss/ne-vss-vss_restore_type">VSS_RESTORE_TYPE</a> enumeration value indicating the type of restore to be performed.

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
Successfully set the backup state.

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
The backup components object is not initialized, this method has been called during a backup operation, or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
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

## -remarks

Typically, most restore operations will not need to override the default restore type (VSS_RTYPE_UNDEFINED). Writers should treat this restore type as if it were VSS_RTYPE_BY_COPY.

If applications need to call 
<b>SetRestoreState</b>, it should be called prior to calling 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>.

If 
<b>SetRestoreState</b> is not called prior to <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>, the default restore state () is used.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_restore_type">VSS_RESTORE_TYPE</a>