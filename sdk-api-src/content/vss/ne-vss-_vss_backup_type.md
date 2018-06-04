---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VSS_BACKUP_TYPE enumeration


## -description


The <b>VSS_BACKUP_TYPE</b> enumeration indicates the 
    type of backup to be performed using VSS writer/requester coordination.


## -enum-fields




### -field VSS_BT_UNDEFINED

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
    (<a href="https://msdn.microsoft.com/41ba60f7-d621-478a-a24a-202d326ebf2c">VSS_FILE_SPEC_BACKUP_TYPE</a>), and designations of 
    files as being part of partial and differenced file operations to select which files must be backed up.

A requester may also use other more traditional techniques to implement an incremental or differential 
    restore, but it must not override the information provided through the VSS interfaces.

If a requester, when processing a given backup type, encounters a writer that does not support that backup 
    type, the requester performs backup or restore operations for that particular writer's data as if the backup type 
    was <b>VSS_BT_FULL</b>.

Requesters set the backup type with a call to 
    <a href="https://msdn.microsoft.com/18a1295d-b763-477b-bda2-baf8a878bf46">IVssBackupComponents::SetBackupState</a>.

Writers use 
    <a href="https://msdn.microsoft.com/b8f78552-27b5-4d64-9d35-baf1c636b526">CVssWriter::GetBackupType</a> to determine the 
    backup type.




## -see-also




<a href="https://msdn.microsoft.com/b8f78552-27b5-4d64-9d35-baf1c636b526">CVssWriter::GetBackupType</a>



<a href="https://msdn.microsoft.com/18a1295d-b763-477b-bda2-baf8a878bf46">IVssBackupComponents::SetBackupState</a>
 

 

