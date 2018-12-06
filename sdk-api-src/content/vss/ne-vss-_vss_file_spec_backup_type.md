---
UID: NE:vss._VSS_FILE_SPEC_BACKUP_TYPE
title: "_VSS_FILE_SPEC_BACKUP_TYPE"
author: windows-sdk-content
description: Used by writers to indicate their support of certain backup operations.
old-location: base\vss_file_spec_backup_type.htm
tech.root: vss
ms.assetid: 41ba60f7-d621-478a-a24a-202d326ebf2c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PVSS_FILE_SPEC_BACKUP_TYPE, PVSS_FILE_SPEC_BACKUP_TYPE, PVSS_FILE_SPEC_BACKUP_TYPE enumeration pointer [VSS], VSS_FILE_SPEC_BACKUP_TYPE, VSS_FILE_SPEC_BACKUP_TYPE enumeration [VSS], VSS_FSBT_ALL_BACKUP_REQUIRED, VSS_FSBT_ALL_SNAPSHOT_REQUIRED, VSS_FSBT_CREATED_DURING_BACKUP, VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED, VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED, VSS_FSBT_FULL_BACKUP_REQUIRED, VSS_FSBT_FULL_SNAPSHOT_REQUIRED, VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED, VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED, VSS_FSBT_LOG_BACKUP_REQUIRED, VSS_FSBT_LOG_SNAPSHOT_REQUIRED, _VSS_FILE_SPEC_BACKUP_TYPE, _win32_vss_file_spec_backup_type, base.vss_file_spec_backup_type, vss/PVSS_FILE_SPEC_BACKUP_TYPE, vss/VSS_FILE_SPEC_BACKUP_TYPE, vss/VSS_FSBT_ALL_BACKUP_REQUIRED, vss/VSS_FSBT_ALL_SNAPSHOT_REQUIRED, vss/VSS_FSBT_CREATED_DURING_BACKUP, vss/VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED, vss/VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED, vss/VSS_FSBT_FULL_BACKUP_REQUIRED, vss/VSS_FSBT_FULL_SNAPSHOT_REQUIRED, vss/VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED, vss/VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED, vss/VSS_FSBT_LOG_BACKUP_REQUIRED, vss/VSS_FSBT_LOG_SNAPSHOT_REQUIRED"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_FILE_SPEC_BACKUP_TYPE
product: Windows
targetos: Windows
req.typenames: VSS_FILE_SPEC_BACKUP_TYPE, *PVSS_FILE_SPEC_BACKUP_TYPE
req.redist: 
---

# _VSS_FILE_SPEC_BACKUP_TYPE enumeration


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




### -field VSS_FSBT_FULL_BACKUP_REQUIRED

A file set tagged with this value must be involved in all types of backup operations. 
     

A writer tags a file set with this value to indicate to the requester that it expects a copy of the current 
      version of the file set to be available following the restore of any backup operation with a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_FULL</b>.


### -field VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED

A writer tags a file set with this value to indicate to the requester that it expects a copy of the current 
      version of the file set to be available following the restore of any backup operation with a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_DIFFERENTIAL</b>.

This value is not supported for express writers.


### -field VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED

A writer tags a file set with this value to indicate to the requester that it expects a copy of the current 
      version of the file set to be available following the restore of any backup operation with a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_INCREMENTAL</b>.

This value is not supported for express writers.


### -field VSS_FSBT_LOG_BACKUP_REQUIRED

A writer tags a file set with this value to indicate to the requester that it expects a copy of the current 
      version of the file set to be available following the restore of any backup operation with a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_LOG</b>.

This value is not supported for express writers.


### -field VSS_FSBT_FULL_SNAPSHOT_REQUIRED

A file set tagged with this value must be backed up from a shadow copy of a volume (and never from the 
      original volume) when participating in a backup operation with a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_FULL</b>.


### -field VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED

A file set tagged with this value must be backed up from a shadow copy of a volume (and never from the 
      original volume) when participating in a backup operation with a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_DIFFERENTIAL</b>.


### -field VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED

A file set tagged with this value must be backed up from a shadow copy of a volume (and never from the 
      original volume) when participating in a backup operation with a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_INCREMENTAL</b>.


### -field VSS_FSBT_LOG_SNAPSHOT_REQUIRED

A file set tagged with this value must be backed up from a shadow copy of a volume (and never from the 
      original volume) when participating in a backup operation with a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> of 
      <b>VSS_BT_LOG</b>).


### -field VSS_FSBT_CREATED_DURING_BACKUP

A writer tags a file set with this value to indicate to the requester that they expect the file to be created during the snapshot sequence.


### -field VSS_FSBT_ALL_BACKUP_REQUIRED

The default file backup specification type. A file set tagged with this value must always participate in 
      backup and restore operations.


### -field VSS_FSBT_ALL_SNAPSHOT_REQUIRED

The shadow copy requirement for backup. A file set tagged with this value must always be backed up from a 
      shadow copy of a volume (and never from the original volume) when participating in a backup operation.


## -remarks



When a writer sets a backup-required value of the 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> enumeration, it is 
    indicating that the requester perform the backup in such a way that, when the backup is restored, the current 
    version of the file set is restored. Typically, this means that the file set is copied as part of the backup.

This setting can be overridden if a file is added to the Backup Components Document as a differenced file 
    (using 
    <a href="https://msdn.microsoft.com/33372d10-c947-45de-9ea2-03ba6378179d">IVssComponent::AddDifferencedFilesByLastModifyTime</a>) 
    or as a partial file (using 
    <a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">IVssComponent::AddPartialFile</a>).

If a file is added as a differenced file, the writer establishes criteria by which the requester should decide 
    whether or not to actually copy a file to a backup medium. A writer typically adds differenced files to the Backup 
    Components Document for inclusion in a backup 
    <a href="vssgloss_p.htm">PostSnapshot</a> event (see 
    <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>). See 
    <a href="https://msdn.microsoft.com/e9529aad-cf93-4b4c-811c-0ff0b708de6c">Incremental and Differential Backups</a> 
    for details.

When a writer sets a shadow copy-required value of the 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> enumeration, it 
    indicates that the file set should be backed up from a shadow-copied volume. File sets not tagged with a 
    shadow copy-required value can be backed up from the original volume.

Writers set <b>VSS_FILE_SPEC_BACKUP_TYPE</b> values 
    while handling an <a href="vssgloss_i.htm">Identify</a> event (see 
    <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">CVssWriter::OnIdentify</a>).

A bit mask (or bitwise OR) of 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> values can be applied 
    to a file set when adding it to a component using the 
    <a href="https://msdn.microsoft.com/5d5a0155-467c-4c42-876e-a1b245cf6f8e">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
    <a href="https://msdn.microsoft.com/37ef5e50-127d-4bd0-9d26-04dc7781b3ff">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
    <a href="https://msdn.microsoft.com/09bdbdf3-d757-4d3c-8b8b-f792b6cd4ef1">IVssCreateWriterMetadata::AddDatabaseLogFiles</a> 
    method.

If no explicit file specification backup type is supplied during the addition of a file specification to a 
    component, the specification is tagged with the default 
    <b>VSS_FILE_SPEC_BACKUP_TYPE</b> value:
    (VSS_FSBT_ALL_BACKUP_REQUIRED | VSS_FSBT_ALL_SNAPSHOT_REQUIRED).

Requesters or writers can recover a file set's file specification backup type by using the 
    <a href="https://msdn.microsoft.com/9d5f3a16-2053-42dd-867d-740c4a34bdb6">IVssWMFiledesc::GetBackupTypeMask</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/33372d10-c947-45de-9ea2-03ba6378179d">IVssComponent::AddDifferencedFilesByLastModifyTime</a>



<a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">IVssComponent::AddPartialFile</a>



<a href="https://msdn.microsoft.com/37ef5e50-127d-4bd0-9d26-04dc7781b3ff">IVssCreateWriterMetadata::AddDatabaseFiles</a>



<a href="https://msdn.microsoft.com/09bdbdf3-d757-4d3c-8b8b-f792b6cd4ef1">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>



<a href="https://msdn.microsoft.com/5d5a0155-467c-4c42-876e-a1b245cf6f8e">IVssCreateWriterMetadata::AddFilesToFileGroup</a>



<a href="https://msdn.microsoft.com/9d5f3a16-2053-42dd-867d-740c4a34bdb6">IVssWMFiledesc::GetBackupTypeMask</a>



<a href="https://msdn.microsoft.com/e9529aad-cf93-4b4c-811c-0ff0b708de6c">Incremental and Differential Backups</a>
 

 

