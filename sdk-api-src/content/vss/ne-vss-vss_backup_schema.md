---
UID: NE:vss._VSS_BACKUP_SCHEMA
title: VSS_BACKUP_SCHEMA (vss.h)
description: Used by a writer to indicate the types of backup operations it can participate in.
helpviewer_keywords: ["*PVSS_BACKUP_SCHEMA","PVSS_BACKUP_SCHEMA","PVSS_BACKUP_SCHEMA enumeration pointer [VSS]","VSS_BACKUP_SCHEMA","VSS_BACKUP_SCHEMA enumeration [VSS]","VSS_BS_AUTHORITATIVE_RESTORE","VSS_BS_COPY","VSS_BS_DIFFERENTIAL","VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL","VSS_BS_INCREMENTAL","VSS_BS_INDEPENDENT_SYSTEM_STATE","VSS_BS_LAST_MODIFY","VSS_BS_LOG","VSS_BS_LSN","VSS_BS_RESTORE_RENAME","VSS_BS_ROLLFORWARD_RESTORE","VSS_BS_TIMESTAMPED","VSS_BS_UNDEFINED","VSS_BS_WRITER_SUPPORTS_NEW_TARGET","VSS_BS_WRITER_SUPPORTS_PARALLEL_RESTORES","VSS_BS_WRITER_SUPPORTS_RESTORE_WITH_MOVE","_win32_vss_backup_schema","base.vss_backup_schema","vss/PVSS_BACKUP_SCHEMA","vss/VSS_BACKUP_SCHEMA","vss/VSS_BS_AUTHORITATIVE_RESTORE","vss/VSS_BS_COPY","vss/VSS_BS_DIFFERENTIAL","vss/VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL","vss/VSS_BS_INCREMENTAL","vss/VSS_BS_INDEPENDENT_SYSTEM_STATE","vss/VSS_BS_LAST_MODIFY","vss/VSS_BS_LOG","vss/VSS_BS_LSN","vss/VSS_BS_RESTORE_RENAME","vss/VSS_BS_ROLLFORWARD_RESTORE","vss/VSS_BS_TIMESTAMPED","vss/VSS_BS_UNDEFINED","vss/VSS_BS_WRITER_SUPPORTS_NEW_TARGET","vss/VSS_BS_WRITER_SUPPORTS_PARALLEL_RESTORES","vss/VSS_BS_WRITER_SUPPORTS_RESTORE_WITH_MOVE"]
old-location: base\vss_backup_schema.htm
tech.root: base
ms.assetid: 3541c8bd-2712-458b-9153-1fffe6bf5688
ms.date: 12/05/2018
ms.keywords: '*PVSS_BACKUP_SCHEMA, PVSS_BACKUP_SCHEMA, PVSS_BACKUP_SCHEMA enumeration pointer [VSS], VSS_BACKUP_SCHEMA, VSS_BACKUP_SCHEMA enumeration [VSS], VSS_BS_AUTHORITATIVE_RESTORE, VSS_BS_COPY, VSS_BS_DIFFERENTIAL, VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL, VSS_BS_INCREMENTAL, VSS_BS_INDEPENDENT_SYSTEM_STATE, VSS_BS_LAST_MODIFY, VSS_BS_LOG, VSS_BS_LSN, VSS_BS_RESTORE_RENAME, VSS_BS_ROLLFORWARD_RESTORE, VSS_BS_TIMESTAMPED, VSS_BS_UNDEFINED, VSS_BS_WRITER_SUPPORTS_NEW_TARGET, VSS_BS_WRITER_SUPPORTS_PARALLEL_RESTORES, VSS_BS_WRITER_SUPPORTS_RESTORE_WITH_MOVE, _win32_vss_backup_schema, base.vss_backup_schema, vss/PVSS_BACKUP_SCHEMA, vss/VSS_BACKUP_SCHEMA, vss/VSS_BS_AUTHORITATIVE_RESTORE, vss/VSS_BS_COPY, vss/VSS_BS_DIFFERENTIAL, vss/VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL, vss/VSS_BS_INCREMENTAL, vss/VSS_BS_INDEPENDENT_SYSTEM_STATE, vss/VSS_BS_LAST_MODIFY, vss/VSS_BS_LOG, vss/VSS_BS_LSN, vss/VSS_BS_RESTORE_RENAME, vss/VSS_BS_ROLLFORWARD_RESTORE, vss/VSS_BS_TIMESTAMPED, vss/VSS_BS_UNDEFINED, vss/VSS_BS_WRITER_SUPPORTS_NEW_TARGET, vss/VSS_BS_WRITER_SUPPORTS_PARALLEL_RESTORES, vss/VSS_BS_WRITER_SUPPORTS_RESTORE_WITH_MOVE'
req.header: vss.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_BACKUP_SCHEMA, *PVSS_BACKUP_SCHEMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_BACKUP_SCHEMA
 - vss/_VSS_BACKUP_SCHEMA
 - PVSS_BACKUP_SCHEMA
 - vss/PVSS_BACKUP_SCHEMA
 - VSS_BACKUP_SCHEMA
 - vss/VSS_BACKUP_SCHEMA
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
 - VSS_BACKUP_SCHEMA
---

# VSS_BACKUP_SCHEMA enumeration


## -description

The <b>VSS_BACKUP_SCHEMA</b> enumeration is used by 
    a writer to indicate the types of backup operations it can participate in. The supported kinds of 
    backup are expressed as a bit mask (or bitwise OR) of 
    <b>VSS_BACKUP_SCHEMA</b> values.

## -enum-fields

### -field VSS_BS_UNDEFINED:0

The writer supports a simple full backup and restoration of entire files (as defined by a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> value of 
      <b>VSS_BT_FULL</b>). This backup scheme can be used as the basis of an incremental or 
      differential backup. This is the default value.

### -field VSS_BS_DIFFERENTIAL:0x1

The writer supports differential backups (corresponding to the 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> value 
      <b>VSS_BT_DIFFERENTIAL</b>). Files created or changed since the last full backup are saved. 
      Files are not marked as having been backed up.
      

This setting does not preclude mixing of incremental and differential backups.

This value is not supported for express writers.

### -field VSS_BS_INCREMENTAL:0x2

The writer supports incremental backups (corresponding to the 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> value 
      <b>VSS_BT_INCREMENTAL</b>). Files created or changed since the last full or incremental 
      backup are saved. Files are marked as having been backed up. 
      

This setting does not preclude mixing of incremental and differential backups.

This value is not supported for express writers.

### -field VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL:0x4

The writer supports both differential and incremental backup schemas, but only exclusively: for example, 
      you cannot follow a differential backup with an incremental one. A writer cannot support this schema if it does 
      not support both incremental and differential schemas (<b>VSS_BS_DIFFERENTIAL</b> | 
      <b>VSS_BS_INCREMENTAL</b>).

This value is not supported for express writers.

### -field VSS_BS_LOG:0x8

The writer supports backups that involve only the log files it manages (corresponding to a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> value of 
      <b>VSS_BT_LOG</b>). This schema requires a writer to have added at least one file to at 
      least one component using the 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDataBaseLogFiles</a> 
      method. Requesters retrieve log file information using the 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile">IVssWMComponent::GetDatabaseLogFile</a> 
      method.

### -field VSS_BS_COPY:0x10

Similar to the default backup schema (<b>VSS_BT_UNDEFINED</b>), the writer supports 
      copy backup operations (corresponding to <b>VSS_BT_COPY</b>) where file access information 
      (such as information as to when a file was last backed up) will not be updated either in the writer's own state 
      information or in the file system information. This type of backup cannot be used as the basis of an incremental 
      or differential backup.

### -field VSS_BS_TIMESTAMPED:0x20

A writer supports using the VSS time-stamp mechanism when evaluating if a file should be included in 
      differential or incremental operations (corresponding to <b>VSS_BT_DIFFERENTIAL</b> and 
      <b>VSS_BT_INCREMENTAL</b>, respectively) using the 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupstamp">IVssComponent::GetBackupStamp</a>, 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp">IVssComponent::GetPreviousBackupStamp</a>, 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a>, and 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp">IVssBackupComponents::SetPreviousBackupStamp</a> 
      methods. 
      

A writer cannot support this schema if it does not support either differential or incremental backup schemas 
       (<b>VSS_BS_DIFFERENTIAL</b> or <b>VSS_BS_INCREMENTAL</b>).

This value is not supported for express writers.

### -field VSS_BS_LAST_MODIFY:0x40

When implementing incremental or differential backups with differenced files, a writer can provide last 
      modification time information for files (using 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a>). 
      A requester then can use 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfile">IVssComponent::GetDifferencedFile</a> to 
      obtain candidate files and information about their last modification data. The requester can use this 
      information (along with any records about previous backup operations it maintains) to decide if a file should be 
      included in incremental and differential backups. 
      

This scheme does not apply to partial file implementations of incremental and differential backup 
       operations.

A writer cannot support this schema if it does not support either incremental or differential backup schemas 
       (<b>VSS_BS_DIFFERENTIAL</b> or <b>VSS_BS_INCREMENTAL</b>).

This value is not supported for express writers.

### -field VSS_BS_LSN:0x80

Reserved for system use.

### -field VSS_BS_WRITER_SUPPORTS_NEW_TARGET:0x100

The writer supports a requester changing the target for file restoration using 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addnewtarget">IVssBackupComponents::AddNewTarget</a>. 
      (See <a href="/windows/desktop/VSS/non-default-backup-and-restore-locations">Non-Default Backup And Restore 
      Locations</a> for more information.)

This value is not supported for express writers.

### -field VSS_BS_WRITER_SUPPORTS_RESTORE_WITH_MOVE:0x200

The writer supports running multiple writer instances with the same class ID, and it supports a requester moving a component to a different writer instance at restore time using <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex">IVssBackupComponentsEx::SetSelectedForRestoreEx</a>.
      

This value is not supported for express writers.

<b>Windows Server 2003:  </b>This value is not supported until Windows Server 2003 with SP1.

### -field VSS_BS_INDEPENDENT_SYSTEM_STATE:0x400

The writer supports backing up data that is part of the system state, but that can also be backed up independently of the system state.

<b>Windows Server 2003:  </b>This value is not supported until Windows Vista.

### -field VSS_BS_ROLLFORWARD_RESTORE:0x1000

The writer supports a requester setting a roll-forward restore point using <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward">IVssBackupComponentsEx2::SetRollForward</a>.

This value is not supported for express writers.

<b>Windows Server 2003:  </b>This value is not supported until Windows Vista.

### -field VSS_BS_RESTORE_RENAME:0x2000

The writer supports a requester setting a restore name using <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename">IVssBackupComponentsEx2::SetRestoreName</a>.

This value is not supported for express writers.

<b>Windows Server 2003:  </b>This value is not supported until Windows Vista.

### -field VSS_BS_AUTHORITATIVE_RESTORE:0x4000

The writer supports a requester setting authoritative restore using <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore">IVssBackupComponentsEx2::SetAuthoritativeRestore</a>.

This value is not supported for express writers.

<b>Windows Server 2003:  </b>This value is not supported until Windows Vista.

### -field VSS_BS_WRITER_SUPPORTS_PARALLEL_RESTORES:0x8000

The writer supports multiple unsynchronized restore events.

This value is not supported for express writers.

<b>Windows Vista and Windows Server 2003:  </b>This value is not supported until Windows Server 2008.

## -remarks

Writer set their backup schemas with calls to 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema">IVssCreateWriterMetadata::SetBackupSchema</a>.

Requesters use 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema">IVssExamineWriterMetadata::GetBackupSchema</a> 
    to determine the backup schema that a writer supports.

For a specific kind of backup operation to be supported, the writer must support the corresponding schema, and 
    the requester must set the corresponding backup type.

For example, to involve a writer in an incremental backup operation, the requester must set the backup type to 
    <b>VSS_BT_INCREMENTAL</b>, and the writer should have a backup schema that includes <b>VSS_BS_INCREMENTAL</b>.

A writer that does not support the backup schema corresponding to a requester's backup type should treat the backup operation that is being performed as if it were a default (full) backup. If the desired backup type is not supported by the writer's backup schema, the requester can either perform a full backup for this writer or exclude the writer from the backup operation. A requester can exclude a writer by selecting none of the writer's components (see 
    <a href="/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with Selectability and 
    Logical Paths</a>), or by disabling the writer (see 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses">IVssBackupComponents::DisableWriterClasses</a> or 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances">IVssBackupComponents::DisableWriterInstances</a>).

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">IVssBackupComponents::SetBackupState</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore">IVssBackupComponentsEx2::SetAuthoritativeRestore</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename">IVssBackupComponentsEx2::SetRestoreName</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward">IVssBackupComponentsEx2::SetRollForward</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex">IVssBackupComponentsEx::SetSelectedForRestoreEx</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-addpartialfile">IVssComponent::AddPartialFile</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema">IVssCreateWriterMetadata::SetBackupSchema</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema">IVssExamineWriterMetadata::GetBackupSchema</a>



<a href="/windows/desktop/VSS/incremental-and-differential-backups">Incremental and Differential Backups</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_flags">VSS_COMPONENT_FLAGS</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a>
