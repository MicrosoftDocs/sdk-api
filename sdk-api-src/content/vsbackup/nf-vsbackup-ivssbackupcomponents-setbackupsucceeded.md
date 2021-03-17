---
UID: NF:vsbackup.IVssBackupComponents.SetBackupSucceeded
title: IVssBackupComponents::SetBackupSucceeded (vsbackup.h)
description: The SetBackupSucceeded method indicates whether the backup of the specified component of a specific writer was successful.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetBackupSucceeded method","IVssBackupComponents.SetBackupSucceeded","IVssBackupComponents::SetBackupSucceeded","SetBackupSucceeded","SetBackupSucceeded method [VSS]","SetBackupSucceeded method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setbackupsucceeded","base.ivssbackupcomponents_setbackupsucceeded","vsbackup/IVssBackupComponents::SetBackupSucceeded"]
old-location: base\ivssbackupcomponents_setbackupsucceeded.htm
tech.root: base
ms.assetid: 5565183d-f374-4796-a399-b008041afdd2
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetBackupSucceeded method, IVssBackupComponents.SetBackupSucceeded, IVssBackupComponents::SetBackupSucceeded, SetBackupSucceeded, SetBackupSucceeded method [VSS], SetBackupSucceeded method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setbackupsucceeded, base.ivssbackupcomponents_setbackupsucceeded, vsbackup/IVssBackupComponents::SetBackupSucceeded
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
 - IVssBackupComponents::SetBackupSucceeded
 - vsbackup/IVssBackupComponents::SetBackupSucceeded
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
 - IVssBackupComponents.SetBackupSucceeded
---

# IVssBackupComponents::SetBackupSucceeded


## -description

The 
<b>SetBackupSucceeded</b> method indicates whether the backup of the specified component of a specific writer was successful.

## -parameters

### -param instanceId [in]

Globally unique identifier (GUID) of the writer instance.

### -param writerId [in]

Globally unique identifier (GUID) of the writer class.

### -param ct [in]

Type of the component. See 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> for the possible values.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component. 


For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component. 




The string cannot be <b>NULL</b> and should contain the same component name as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

### -param bSucceded [in]

Set this parameter to <b>true</b> if the component was successfully backed up, or <b>false</b> otherwise.

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
Successfully set the backup succeeded state.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The backup component does not exist.

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

When working in component mode (when 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a> is called with its select components argument set to <b>true</b>), writers check the state of each components backup using 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupsucceeded">IVssComponent::GetBackupSucceeded</a>. Therefore, a well-behaved backup application (requester) must call 
<b>SetBackupSucceeded</b> after each component has been processed and prior to calling 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">IVssBackupComponents::BackupComplete</a>.

Do not call this method if the call to <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a> failed.  For more information about how requesters use  <b>DoSnapshotSet</b>, <b>SetBackupSucceeded</b>, and <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> in a backup operation, see <a href="/windows/desktop/VSS/overview-of-pre-backup-tasks">Overview of Pre-Backup Tasks</a> and <a href="/windows/desktop/VSS/overview-of-actual-backup-of-files">Overview of Actual Backup Of Files</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">IVssBackupComponents::BackupComplete</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>