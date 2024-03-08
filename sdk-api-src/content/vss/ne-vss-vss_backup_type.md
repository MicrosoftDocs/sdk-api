---
UID: NE:vss._VSS_BACKUP_TYPE
title: VSS_BACKUP_TYPE (vss.h)
description: Indicates the type of backup to be performed.
helpviewer_keywords: ["*PVSS_BACKUP_TYPE","PVSS_BACKUP_TYPE","PVSS_BACKUP_TYPE enumeration pointer [VSS]","VSS_BACKUP_TYPE","VSS_BACKUP_TYPE enumeration [VSS]","VSS_BT_COPY","VSS_BT_DIFFERENTIAL","VSS_BT_FULL","VSS_BT_INCREMENTAL","VSS_BT_LOG","VSS_BT_OTHER","VSS_BT_UNDEFINED","_win32_vss_backup_type","base.vss_backup_type","vss/PVSS_BACKUP_TYPE","vss/VSS_BACKUP_TYPE","vss/VSS_BT_COPY","vss/VSS_BT_DIFFERENTIAL","vss/VSS_BT_FULL","vss/VSS_BT_INCREMENTAL","vss/VSS_BT_LOG","vss/VSS_BT_OTHER","vss/VSS_BT_UNDEFINED"]
old-location: base\vss_backup_type.htm
tech.root: base
ms.assetid: 82934737-0d80-4b5d-a1fa-1ba38e446504
ms.date: 12/05/2018
ms.keywords: '*PVSS_BACKUP_TYPE, PVSS_BACKUP_TYPE, PVSS_BACKUP_TYPE enumeration pointer [VSS], VSS_BACKUP_TYPE, VSS_BACKUP_TYPE enumeration [VSS], VSS_BT_COPY, VSS_BT_DIFFERENTIAL, VSS_BT_FULL, VSS_BT_INCREMENTAL, VSS_BT_LOG, VSS_BT_OTHER, VSS_BT_UNDEFINED, _win32_vss_backup_type, base.vss_backup_type, vss/PVSS_BACKUP_TYPE, vss/VSS_BACKUP_TYPE, vss/VSS_BT_COPY, vss/VSS_BT_DIFFERENTIAL, vss/VSS_BT_FULL, vss/VSS_BT_INCREMENTAL, vss/VSS_BT_LOG, vss/VSS_BT_OTHER, vss/VSS_BT_UNDEFINED'
req.header: vss.h
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
req.typenames: VSS_BACKUP_TYPE, *PVSS_BACKUP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_BACKUP_TYPE
 - vss/_VSS_BACKUP_TYPE
 - PVSS_BACKUP_TYPE
 - vss/PVSS_BACKUP_TYPE
 - VSS_BACKUP_TYPE
 - vss/VSS_BACKUP_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_BACKUP_TYPE
---

# VSS_BACKUP_TYPE enumeration


## -description

The <b>VSS_BACKUP_TYPE</b> enumeration indicates the 
    type of backup to be performed using VSS writer/requester coordination.

## -enum-fields

### -field VSS_BT_UNDEFINED:0

The backup type is not known. 
      

This value indicates an application error.

### -field VSS_BT_FULL

Full backup: all files, regardless of whether they have been marked as backed up or not, are saved. This is 
      the default backup type and schema, and all writers support it. 
      

Each file's backup history will be updated to reflect that it was backed up.

### -field VSS_BT_INCREMENTAL

Incremental backup: files created or changed since the last full or incremental backup are saved. Files are 
      marked as having been backed up. 
      

A requester can implement this sort of backup on a particular writer only if it supports the 
       <b>VSS_BS_INCREMENTAL</b> schema.

If a requester's backup type is <b>VSS_BT_INCREMENTAL</b> and a particular writer's 
       backup schema does not support that sort of backup, the requester will always perform a full 
       (<b>VSS_BT_FULL</b>) backup on that writer's data.

### -field VSS_BT_DIFFERENTIAL

Differential backup: files created or changed since the last full backup are saved. Files are not marked as 
      having been backed up. 
      

A requester can implement this sort of backup on a particular writer only if it supports the
       <b>VSS_BS_DIFFERENTIAL</b> schema.

If a requester's backup type is <b>VSS_BT_DIFFERENTIAL</b> and a particular writer's 
       backup schema does not support that sort of backup, the requester will always perform a full 
       (<b>VSS_BT_FULL</b>) backup on that writer's data.

### -field VSS_BT_LOG

The log file of a writer is to participate in backup or restore operations. 
      

A requester can implement this sort of backup on a particular writer only if it supports the 
       <b>VSS_BS_LOG</b> schema.

If a requester's backup type is <b>VSS_BT_LOG</b> and a particular writer's backup 
       schema does not support that sort of backup, the requester will always perform a full 
       (<b>VSS_BT_FULL</b>) backup on that writer's data.

### -field VSS_BT_COPY

Files on disk will be copied to a backup medium regardless of the state of each file's backup history, and 
      the backup history will not be updated. 
      

A requester can implement this sort of backup on a particular writer only if it supports the 
       <b>VSS_BS_COPY</b> schema.

If a requester's backup type is <b>VSS_BT_COPY</b> and a particular writer's backup 
       schema does not support that sort of backup, the requester will always perform a full 
       (<b>VSS_BT_FULL</b>) backup on that writer's data.

### -field VSS_BT_OTHER

Backup type that is not full, copy, log, incremental, or differential.

## -remarks

An implementation of a backup type defined by a 
    <b>VSS_BACKUP_TYPE</b> value must be done using the VSS API.

This is particularly true in the case of incremental (<b>VSS_BT_INCREMENTAL</b>) and 
    differential (<b>VSS_BT_DIFFERENTIAL</b>) backups. In these cases, requesters and writers 
    work together using the file backup specification masks 
    (<a href="/windows/desktop/api/vss/ne-vss-vss_file_spec_backup_type">VSS_FILE_SPEC_BACKUP_TYPE</a>), and designations of 
    files as being part of partial and differenced file operations to select which files must be backed up.

A requester may also use other more traditional techniques to implement an incremental or differential 
    restore, but it must not override the information provided through the VSS interfaces.

If a requester, when processing a given backup type, encounters a writer that does not support that backup 
    type, the requester performs backup or restore operations for that particular writer's data as if the backup type 
    was <b>VSS_BT_FULL</b>.

Requesters set the backup type with a call to 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a>.

Writers use 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getbackuptype">CVssWriter::GetBackupType</a> to determine the 
    backup type.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getbackuptype">CVssWriter::GetBackupType</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a>
