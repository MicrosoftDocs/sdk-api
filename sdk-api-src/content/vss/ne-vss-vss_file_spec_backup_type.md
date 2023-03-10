---
UID: NE:vss._VSS_FILE_SPEC_BACKUP_TYPE
title: VSS_FILE_SPEC_BACKUP_TYPE (vss.h)
description: Used by writers to indicate their support of certain backup operations.
helpviewer_keywords: ["*PVSS_FILE_SPEC_BACKUP_TYPE","PVSS_FILE_SPEC_BACKUP_TYPE","PVSS_FILE_SPEC_BACKUP_TYPE enumeration pointer [VSS]","VSS_FILE_SPEC_BACKUP_TYPE","VSS_FILE_SPEC_BACKUP_TYPE enumeration [VSS]","VSS_FSBT_ALL_BACKUP_REQUIRED","VSS_FSBT_ALL_SNAPSHOT_REQUIRED","VSS_FSBT_CREATED_DURING_BACKUP","VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED","VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED","VSS_FSBT_FULL_BACKUP_REQUIRED","VSS_FSBT_FULL_SNAPSHOT_REQUIRED","VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED","VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED","VSS_FSBT_LOG_BACKUP_REQUIRED","VSS_FSBT_LOG_SNAPSHOT_REQUIRED","_win32_vss_file_spec_backup_type","base.vss_file_spec_backup_type","vss/PVSS_FILE_SPEC_BACKUP_TYPE","vss/VSS_FILE_SPEC_BACKUP_TYPE","vss/VSS_FSBT_ALL_BACKUP_REQUIRED","vss/VSS_FSBT_ALL_SNAPSHOT_REQUIRED","vss/VSS_FSBT_CREATED_DURING_BACKUP","vss/VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED","vss/VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED","vss/VSS_FSBT_FULL_BACKUP_REQUIRED","vss/VSS_FSBT_FULL_SNAPSHOT_REQUIRED","vss/VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED","vss/VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED","vss/VSS_FSBT_LOG_BACKUP_REQUIRED","vss/VSS_FSBT_LOG_SNAPSHOT_REQUIRED"]
old-location: base\vss_file_spec_backup_type.htm
tech.root: base
ms.assetid: 41ba60f7-d621-478a-a24a-202d326ebf2c
ms.date: 12/05/2018
ms.keywords: '*PVSS_FILE_SPEC_BACKUP_TYPE, PVSS_FILE_SPEC_BACKUP_TYPE, PVSS_FILE_SPEC_BACKUP_TYPE enumeration pointer [VSS], VSS_FILE_SPEC_BACKUP_TYPE, VSS_FILE_SPEC_BACKUP_TYPE enumeration [VSS], VSS_FSBT_ALL_BACKUP_REQUIRED, VSS_FSBT_ALL_SNAPSHOT_REQUIRED, VSS_FSBT_CREATED_DURING_BACKUP, VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED, VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED, VSS_FSBT_FULL_BACKUP_REQUIRED, VSS_FSBT_FULL_SNAPSHOT_REQUIRED, VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED, VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED, VSS_FSBT_LOG_BACKUP_REQUIRED, VSS_FSBT_LOG_SNAPSHOT_REQUIRED, _win32_vss_file_spec_backup_type, base.vss_file_spec_backup_type, vss/PVSS_FILE_SPEC_BACKUP_TYPE, vss/VSS_FILE_SPEC_BACKUP_TYPE, vss/VSS_FSBT_ALL_BACKUP_REQUIRED, vss/VSS_FSBT_ALL_SNAPSHOT_REQUIRED, vss/VSS_FSBT_CREATED_DURING_BACKUP, vss/VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED, vss/VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED, vss/VSS_FSBT_FULL_BACKUP_REQUIRED, vss/VSS_FSBT_FULL_SNAPSHOT_REQUIRED, vss/VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED, vss/VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED, vss/VSS_FSBT_LOG_BACKUP_REQUIRED, vss/VSS_FSBT_LOG_SNAPSHOT_REQUIRED'
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
req.typenames: VSS_FILE_SPEC_BACKUP_TYPE, *PVSS_FILE_SPEC_BACKUP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_FILE_SPEC_BACKUP_TYPE
 - vss/_VSS_FILE_SPEC_BACKUP_TYPE
 - PVSS_FILE_SPEC_BACKUP_TYPE
 - vss/PVSS_FILE_SPEC_BACKUP_TYPE
 - VSS_FILE_SPEC_BACKUP_TYPE
 - vss/VSS_FILE_SPEC_BACKUP_TYPE
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
 - VSS_FILE_SPEC_BACKUP_TYPE
---

# VSS_FILE_SPEC_BACKUP_TYPE enumeration


## -description

The <b>VSS_FILE_SPEC_BACKUP_TYPE</b> enumeration is 
    used by writers to indicate their support of certain backup 
    operations—such as incremental or differential backup—on the 
    basis of file sets (a specified file or files).

File sets stored in the Writer Metadata Document are tagged with a bit mask (or bitwise OR) of 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> values indicating the 
    following:
<ul>
<li>Whether the writer and the requester have to evaluate a given file set for participation in the specified 
     type of backup operations</li>
<li>Whether backing up the specified file will require a shadow copy</li>
</ul>

## -enum-fields

### -field VSS_FSBT_FULL_BACKUP_REQUIRED:0x1

A file set tagged with this value must be involved in all types of backup operations. 
     

A writer tags a file set with this value to indicate to the requester that it expects a copy of the current 
      version of the file set to be available following the restore of any backup operation with a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_FULL</b>.

### -field VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED:0x2

A writer tags a file set with this value to indicate to the requester that it expects a copy of the current 
      version of the file set to be available following the restore of any backup operation with a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_DIFFERENTIAL</b>.

This value is not supported for express writers.

### -field VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED:0x4

A writer tags a file set with this value to indicate to the requester that it expects a copy of the current 
      version of the file set to be available following the restore of any backup operation with a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_INCREMENTAL</b>.

This value is not supported for express writers.

### -field VSS_FSBT_LOG_BACKUP_REQUIRED:0x8

A writer tags a file set with this value to indicate to the requester that it expects a copy of the current 
      version of the file set to be available following the restore of any backup operation with a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_LOG</b>.

This value is not supported for express writers.

### -field VSS_FSBT_FULL_SNAPSHOT_REQUIRED:0x100

A file set tagged with this value must be backed up from a shadow copy of a volume (and never from the 
      original volume) when participating in a backup operation with a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_FULL</b>.

### -field VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED:0x200

A file set tagged with this value must be backed up from a shadow copy of a volume (and never from the 
      original volume) when participating in a backup operation with a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_DIFFERENTIAL</b>.

### -field VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED:0x400

A file set tagged with this value must be backed up from a shadow copy of a volume (and never from the 
      original volume) when participating in a backup operation with a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_INCREMENTAL</b>.

### -field VSS_FSBT_LOG_SNAPSHOT_REQUIRED:0x800

A file set tagged with this value must be backed up from a shadow copy of a volume (and never from the 
      original volume) when participating in a backup operation with a 
      <a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_LOG</b>).

### -field VSS_FSBT_CREATED_DURING_BACKUP:0x10000

A writer tags a file set with this value to indicate to the requester that they expect the file to be created during the snapshot sequence.

### -field VSS_FSBT_ALL_BACKUP_REQUIRED:0xf

The default file backup specification type. A file set tagged with this value must always participate in 
      backup and restore operations.

### -field VSS_FSBT_ALL_SNAPSHOT_REQUIRED:0xf00

The shadow copy requirement for backup. A file set tagged with this value must always be backed up from a 
      shadow copy of a volume (and never from the original volume) when participating in a backup operation.

## -remarks

When a writer sets a backup-required value of the 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> enumeration, it is 
    indicating that the requester perform the backup in such a way that, when the backup is restored, the current 
    version of the file set is restored. Typically, this means that the file set is copied as part of the backup.

This setting can be overridden if a file is added to the Backup Components Document as a differenced file 
    (using 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a>) 
    or as a partial file (using 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-addpartialfile">IVssComponent::AddPartialFile</a>).

If a file is added as a differenced file, the writer establishes criteria by which the requester should decide 
    whether or not to actually copy a file to a backup medium. A writer typically adds differenced files to the Backup 
    Components Document for inclusion in a backup 
    <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> event (see 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>). See 
    <a href="/windows/desktop/VSS/incremental-and-differential-backups">Incremental and Differential Backups</a> 
    for details.

When a writer sets a shadow copy-required value of the 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> enumeration, it 
    indicates that the file set should be backed up from a shadow-copied volume. File sets not tagged with a 
    shadow copy-required value can be backed up from the original volume.

Writers set <b>VSS_FILE_SPEC_BACKUP_TYPE</b> values 
    while handling an <a href="/windows/desktop/VSS/vssgloss-i">Identify</a> event (see 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a>).

A bit mask (or bitwise OR) of 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> values can be applied 
    to a file set when adding it to a component using the 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a> 
    method.

If no explicit file specification backup type is supplied during the addition of a file specification to a 
    component, the specification is tagged with the default 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> value:
    (VSS_FSBT_ALL_BACKUP_REQUIRED | VSS_FSBT_ALL_SNAPSHOT_REQUIRED).

Requesters or writers can recover a file set's file specification backup type by using the 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask">IVssWMFiledesc::GetBackupTypeMask</a> 
    method.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-addpartialfile">IVssComponent::AddPartialFile</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask">IVssWMFiledesc::GetBackupTypeMask</a>



<a href="/windows/desktop/VSS/incremental-and-differential-backups">Incremental and Differential Backups</a>
