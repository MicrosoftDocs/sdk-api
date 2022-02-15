---
UID: NE:vswriter.VSS_FILE_RESTORE_STATUS
title: VSS_FILE_RESTORE_STATUS (vswriter.h)
description: Defines the set of statuses of a file restore operation.
helpviewer_keywords: ["VSS_FILE_RESTORE_STATUS","VSS_FILE_RESTORE_STATUS enumeration [VSS]","VSS_RS_ALL","VSS_RS_FAILED","VSS_RS_NONE","VSS_RS_UNDEFINED","_win32_vss_file_restore_status","base.vss_file_restore_status","enumeration [VSS]","vswriter/VSS_FILE_RESTORE_STATUS","vswriter/VSS_RS_ALL","vswriter/VSS_RS_FAILED","vswriter/VSS_RS_NONE","vswriter/VSS_RS_UNDEFINED"]
old-location: base\vss_file_restore_status.htm
tech.root: base
ms.assetid: e1754fad-8da1-4a3e-a70a-ada37dde1c5d
ms.date: 12/05/2018
ms.keywords: VSS_FILE_RESTORE_STATUS, VSS_FILE_RESTORE_STATUS enumeration [VSS], VSS_RS_ALL, VSS_RS_FAILED, VSS_RS_NONE, VSS_RS_UNDEFINED, _win32_vss_file_restore_status, base.vss_file_restore_status, enumeration [VSS], vswriter/VSS_FILE_RESTORE_STATUS, vswriter/VSS_RS_ALL, vswriter/VSS_RS_FAILED, vswriter/VSS_RS_NONE, vswriter/VSS_RS_UNDEFINED
req.header: vswriter.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_FILE_RESTORE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VSS_FILE_RESTORE_STATUS
 - vswriter/VSS_FILE_RESTORE_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_FILE_RESTORE_STATUS
---

# VSS_FILE_RESTORE_STATUS enumeration


## -description

The <b>VSS_FILE_RESTORE_STATUS</b> enumeration 
    defines the set of statuses of a file restore operation performed on the files managed by a 
    selected component or component set (see 
    <a href="/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with Selectability and 
    Logical Paths</a> for information on selecting components).

## -enum-fields

### -field VSS_RS_UNDEFINED:0

The restore state is undefined. 
      

This value indicates an error, or indicates that a restore operation has not yet started.

This value is not supported for components that are owned by express writers.

### -field VSS_RS_NONE

No files were restored. 
      

This value indicates an error in restoration that did not leave any restored files on disk.

### -field VSS_RS_ALL

All files were restored. This value indicates success and should be set for each component that was 
      restored successfully.

### -field VSS_RS_FAILED

The restore process failed. 
      

This value indicates an error in restoration that did leave some restored files on disk. This means the 
       components on disk are now corrupt.

## -remarks

If any files managed by a component or, if it defines a component set, any of its subcomponents cannot be 
    restored, the value of <b>VSS_FILE_RESTORE_STATUS</b> 
    must indicate an error.

Both the values <b>VSS_RS_FAILED</b> and <b>VSS_RS_NONE</b> indicate 
    that a restore operation did not complete successfully:

<ul>
<li><b>VSS_RS_NONE</b> indicates a restore failed gracefully: no files from the component 
      or its subcomponents were restored to disk.</li>
<li><b>VSS_RS_FAIL</b> indicates a restore failed gracelessly, leaving some files restored 
      to disk and some files unrestored.</li>
</ul>
Requesters must set a restore status (using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus">IVssBackupComponents::SetFileRestoreStatus</a>) 
    for every component (and its component set, if it defines one) explicitly added for restore to the Backup 
    Components Document (using either 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore">IVssBackupComponents::SetSelectedForRestore</a> or 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent">IVssBackupComponents::AddRestoreSubcomponent</a>).

Writers and requesters can query the status of the restoration of a component or a component set defined by a 
    selectable component with calls to 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus">IVssComponent::GetFileRestoreStatus</a>. If
    this method is called for a component that was not selected, the value returned is undefined.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus">IVssBackupComponents::SetFileRestoreStatus</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus">IVssComponent::GetFileRestoreStatus</a>
