---
UID: NE:vss._VSS_BACKUP_SCHEMA
title: "_VSS_BACKUP_SCHEMA"
author: windows-driver-content
description: Used by a writer to indicate the types of backup operations it can participate in.
old-location: base\vss_backup_schema.htm
old-project: VSS
ms.assetid: 3541c8bd-2712-458b-9153-1fffe6bf5688
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PVSS_BACKUP_SCHEMA, PVSS_BACKUP_SCHEMA, PVSS_BACKUP_SCHEMA enumeration pointer [VSS], VSS_BACKUP_SCHEMA, VSS_BACKUP_SCHEMA enumeration [VSS], VSS_BS_AUTHORITATIVE_RESTORE, VSS_BS_COPY, VSS_BS_DIFFERENTIAL, VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL, VSS_BS_INCREMENTAL, VSS_BS_INDEPENDENT_SYSTEM_STATE, VSS_BS_LAST_MODIFY, VSS_BS_LOG, VSS_BS_LSN, VSS_BS_RESTORE_RENAME, VSS_BS_ROLLFORWARD_RESTORE, VSS_BS_TIMESTAMPED, VSS_BS_UNDEFINED, VSS_BS_WRITER_SUPPORTS_NEW_TARGET, VSS_BS_WRITER_SUPPORTS_PARALLEL_RESTORES, VSS_BS_WRITER_SUPPORTS_RESTORE_WITH_MOVE, _VSS_BACKUP_SCHEMA, _win32_vss_backup_schema, base.vss_backup_schema, vss/PVSS_BACKUP_SCHEMA, vss/VSS_BACKUP_SCHEMA, vss/VSS_BS_AUTHORITATIVE_RESTORE, vss/VSS_BS_COPY, vss/VSS_BS_DIFFERENTIAL, vss/VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL, vss/VSS_BS_INCREMENTAL, vss/VSS_BS_INDEPENDENT_SYSTEM_STATE, vss/VSS_BS_LAST_MODIFY, vss/VSS_BS_LOG, vss/VSS_BS_LSN, vss/VSS_BS_RESTORE_RENAME, vss/VSS_BS_ROLLFORWARD_RESTORE, vss/VSS_BS_TIMESTAMPED, vss/VSS_BS_UNDEFINED, vss/VSS_BS_WRITER_SUPPORTS_NEW_TARGET, vss/VSS_BS_WRITER_SUPPORTS_PARALLEL_RESTORES, vss/VSS_BS_WRITER_SUPPORTS_RESTORE_WITH_MOVE"
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
req.typenames: VSS_BACKUP_SCHEMA, *PVSS_BACKUP_SCHEMA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vss.h
api_name:
-	VSS_BACKUP_SCHEMA
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VSS_BACKUP_SCHEMA enumeration


## -description


The <b>VSS_BACKUP_SCHEMA</b> enumeration is used by 
    a writer to indicate the types of backup operations it can participate in. The supported kinds of 
    backup are expressed as a bit mask (or bitwise OR) of 
    <b>VSS_BACKUP_SCHEMA</b> values.


## -enum-fields




### -field VSS_BS_UNDEFINED

The writer supports a simple full backup and restoration of entire files (as defined by a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> value of 
      <b>VSS_BT_FULL</b>). This backup scheme can be used as the basis of an incremental or 
      differential backup. This is the default value.


### -field VSS_BS_DIFFERENTIAL

The writer supports differential backups (corresponding to the 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> value 
      <b>VSS_BT_DIFFERENTIAL</b>). Files created or changed since the last full backup are saved. 
      Files are not marked as having been backed up.
      

This setting does not preclude mixing of incremental and differential backups.

This value is not supported for express writers.


### -field VSS_BS_INCREMENTAL

The writer supports incremental backups (corresponding to the 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> value 
      <b>VSS_BT_INCREMENTAL</b>). Files created or changed since the last full or incremental 
      backup are saved. Files are marked as having been backed up. 
      

This setting does not preclude mixing of incremental and differential backups.

This value is not supported for express writers.


### -field VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL

The writer supports both differential and incremental backup schemas, but only exclusively: for example, 
      you cannot follow a differential backup with an incremental one. A writer cannot support this schema if it does 
      not support both incremental and differential schemas (<b>VSS_BS_DIFFERENTIAL</b> | 
      <b>VSS_BS_INCREMENTAL</b>).

This value is not supported for express writers.


### -field VSS_BS_LOG

The writer supports backups that involve only the log files it manages (corresponding to a 
      <a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> value of 
      <b>VSS_BT_LOG</b>). This schema requires a writer to have added at least one file to at 
      least one component using the 
      <a href="https://msdn.microsoft.com/09bdbdf3-d757-4d3c-8b8b-f792b6cd4ef1">IVssCreateWriterMetadata::AddDataBaseLogFiles</a> 
      method. Requesters retrieve log file information using the 
      <a href="https://msdn.microsoft.com/8aaab68a-27e3-4e76-8116-530001b504a3">IVssWMComponent::GetDatabaseLogFile</a> 
      method.


### -field VSS_BS_COPY

Similar to the default backup schema (<b>VSS_BT_UNDEFINED</b>), the writer supports 
      copy backup operations (corresponding to <b>VSS_BT_COPY</b>) where file access information 
      (such as information as to when a file was last backed up) will not be updated either in the writer's own state 
      information or in the file system information. This type of backup cannot be used as the basis of an incremental 
      or differential backup.


### -field VSS_BS_TIMESTAMPED

A writer supports using the VSS time-stamp mechanism when evaluating if a file should be included in 
      differential or incremental operations (corresponding to <b>VSS_BT_DIFFERENTIAL</b> and 
      <b>VSS_BT_INCREMENTAL</b>, respectively) using the 
      <a href="https://msdn.microsoft.com/a8f272d8-4024-46bf-a0e6-77d870615fc0">IVssComponent::GetBackupStamp</a>, 
      <a href="https://msdn.microsoft.com/91778854-52af-4e1e-943b-89c786963291">IVssComponent::GetPreviousBackupStamp</a>, 
      <a href="https://msdn.microsoft.com/54995cc9-8988-4f26-9c60-5d809a93e4e1">IVssComponent::SetBackupStamp</a>, and 
      <a href="https://msdn.microsoft.com/cc1c75bf-b281-4741-9273-f7264532860f">IVssBackupComponents::SetPreviousBackupStamp</a> 
      methods. 
      

A writer cannot support this schema if it does not support either differential or incremental backup schemas 
       (<b>VSS_BS_DIFFERENTIAL</b> or <b>VSS_BS_INCREMENTAL</b>).

This value is not supported for express writers.


### -field VSS_BS_LAST_MODIFY

When implementing incremental or differential backups with differenced files, a writer can provide last 
      modification time information for files (using 
      <a href="https://msdn.microsoft.com/33372d10-c947-45de-9ea2-03ba6378179d">IVssComponent::AddDifferencedFilesByLastModifyTime</a>). 
      A requester then can use 
      <a href="https://msdn.microsoft.com/285b2ac7-d09e-4ac5-bf5c-62c510544353">IVssComponent::GetDifferencedFile</a> to 
      obtain candidate files and information about their last modification data. The requester can use this 
      information (along with any records about previous backup operations it maintains) to decide if a file should be 
      included in incremental and differential backups. 
      

This scheme does not apply to partial file implementations of incremental and differential backup 
       operations.

A writer cannot support this schema if it does not support either incremental or differential backup schemas 
       (<b>VSS_BS_DIFFERENTIAL</b> or <b>VSS_BS_INCREMENTAL</b>).

This value is not supported for express writers.


### -field VSS_BS_LSN

Reserved for system use.


### -field VSS_BS_WRITER_SUPPORTS_NEW_TARGET

The writer supports a requester changing the target for file restoration using 
      <a href="https://msdn.microsoft.com/9a4e2638-f6e7-4264-997d-41880f23c981">IVssBackupComponents::AddNewTarget</a>. 
      (See <a href="https://msdn.microsoft.com/7609c392-d5f8-48c2-8e7e-f35f56cf94f8">Non-Default Backup And Restore 
      Locations</a> for more information.)

This value is not supported for express writers.


### -field VSS_BS_WRITER_SUPPORTS_RESTORE_WITH_MOVE

The writer supports running multiple writer instances with the same class ID, and it supports a requester moving a component to a different writer instance at restore time using <a href="https://msdn.microsoft.com/469e6d61-85c6-4385-92be-df6addefe37f">IVssBackupComponentsEx::SetSelectedForRestoreEx</a>.
      

This value is not supported for express writers.

<b>Windows Server 2003:  </b>This value is not supported until Windows Server 2003 with SP1.


### -field VSS_BS_INDEPENDENT_SYSTEM_STATE

The writer supports backing up data that is part of the system state, but that can also be backed up independently of the system state.

<b>Windows Server 2003:  </b>This value is not supported until Windows Vista.


### -field VSS_BS_ROLLFORWARD_RESTORE

The writer supports a requester setting a roll-forward restore point using <a href="https://msdn.microsoft.com/9529284f-2150-4d32-af6c-178ba8681945">IVssBackupComponentsEx2::SetRollForward</a>.

This value is not supported for express writers.

<b>Windows Server 2003:  </b>This value is not supported until Windows Vista.


### -field VSS_BS_RESTORE_RENAME

The writer supports a requester setting a restore name using <a href="https://msdn.microsoft.com/a8334b28-9328-49f4-bf92-f43c556781bf">IVssBackupComponentsEx2::SetRestoreName</a>.

This value is not supported for express writers.

<b>Windows Server 2003:  </b>This value is not supported until Windows Vista.


### -field VSS_BS_AUTHORITATIVE_RESTORE

The writer supports a requester setting authoritative restore using <a href="https://msdn.microsoft.com/3725a282-2df8-4a0a-a1bf-a73c2b259cbf">IVssBackupComponentsEx2::SetAuthoritativeRestore</a>.

This value is not supported for express writers.

<b>Windows Server 2003:  </b>This value is not supported until Windows Vista.


### -field VSS_BS_WRITER_SUPPORTS_PARALLEL_RESTORES

The writer supports multiple unsynchronized restore events.

This value is not supported for express writers.

<b>Windows Vista and Windows Server 2003:  </b>This value is not supported until Windows Server 2008.


## -remarks



Writer set their backup schemas with calls to 
    <a href="https://msdn.microsoft.com/7449fcc8-76fc-4cc5-923c-9a5d53d2cd6b">IVssCreateWriterMetadata::SetBackupSchema</a>.

Requesters use 
    <a href="https://msdn.microsoft.com/d7099d6e-b8dd-44a5-af68-f3347c5d251b">IVssExamineWriterMetadata::GetBackupSchema</a> 
    to determine the backup schema that a writer supports.

For a specific kind of backup operation to be supported, the writer must support the corresponding schema, and 
    the requester must set the corresponding backup type.

For example, to involve a writer in an incremental backup operation, the requester must set the backup type to 
    <b>VSS_BT_INCREMENTAL</b>, and the writer should have a backup schema that includes <b>VSS_BS_INCREMENTAL</b>.

A writer that does not support the backup schema corresponding to a requester's backup type should treat the backup operation that is being performed as if it were a default (full) backup. If the desired backup type is not supported by the writer's backup schema, the requester can either perform a full backup for this writer or exclude the writer from the backup operation. A requester can exclude a writer by selecting none of the writer's components (see 
    <a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability and 
    Logical Paths</a>), or by disabling the writer (see 
    <a href="https://msdn.microsoft.com/7567bf23-4f4c-4210-87f7-4f90262fda7a">IVssBackupComponents::DisableWriterClasses</a> or 
    <a href="https://msdn.microsoft.com/746fb12d-83d7-463d-848d-36e095832d1a">IVssBackupComponents::DisableWriterInstances</a>).




## -see-also




<a href="https://msdn.microsoft.com/18a1295d-b763-477b-bda2-baf8a878bf46">IVssBackupComponents::SetBackupState</a>



<a href="https://msdn.microsoft.com/3725a282-2df8-4a0a-a1bf-a73c2b259cbf">IVssBackupComponentsEx2::SetAuthoritativeRestore</a>



<a href="https://msdn.microsoft.com/a8334b28-9328-49f4-bf92-f43c556781bf">IVssBackupComponentsEx2::SetRestoreName</a>



<a href="https://msdn.microsoft.com/9529284f-2150-4d32-af6c-178ba8681945">IVssBackupComponentsEx2::SetRollForward</a>



<a href="https://msdn.microsoft.com/469e6d61-85c6-4385-92be-df6addefe37f">IVssBackupComponentsEx::SetSelectedForRestoreEx</a>



<a href="https://msdn.microsoft.com/33372d10-c947-45de-9ea2-03ba6378179d">IVssComponent::AddDifferencedFilesByLastModifyTime</a>



<a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">IVssComponent::AddPartialFile</a>



<a href="https://msdn.microsoft.com/7449fcc8-76fc-4cc5-923c-9a5d53d2cd6b">IVssCreateWriterMetadata::SetBackupSchema</a>



<a href="https://msdn.microsoft.com/d7099d6e-b8dd-44a5-af68-f3347c5d251b">IVssExamineWriterMetadata::GetBackupSchema</a>



<a href="https://msdn.microsoft.com/e9529aad-cf93-4b4c-811c-0ff0b708de6c">Incremental and Differential Backups</a>



<a href="https://msdn.microsoft.com/91b7fbab-82f8-48cc-8078-f8f71c48a70b">VSS_COMPONENT_FLAGS</a>



<a href="https://msdn.microsoft.com/31997417-d993-4f28-b108-ce1dd8239650">VSS_USAGE_TYPE</a>
 

 

