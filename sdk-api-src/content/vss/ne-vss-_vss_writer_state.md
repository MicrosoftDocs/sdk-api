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

# _VSS_WRITER_STATE enumeration


## -description


The <b>VSS_WRITER_STATE</b> enumeration indicates the current 
    state of the writer.


## -enum-fields




### -field VSS_WS_UNKNOWN

The writer's state is not known. 
      

This indicates an error on the part of the writer.


### -field VSS_WS_STABLE

The writer has completed processing current shadow copy events and is ready to proceed, or 
      <a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a> has not yet 
      been called.


### -field VSS_WS_WAITING_FOR_FREEZE

The writer is waiting for the freeze state.


### -field VSS_WS_WAITING_FOR_THAW

The writer is waiting for the thaw state.


### -field VSS_WS_WAITING_FOR_POST_SNAPSHOT

The writer is waiting for the 
     <a href="vssgloss_p.htm">PostSnapshot</a> state.


### -field VSS_WS_WAITING_FOR_BACKUP_COMPLETE

The writer is waiting for the requester to finish its backup operation.


### -field VSS_WS_FAILED_AT_IDENTIFY

The writer vetoed the shadow copy creation process at the writer identification state.


### -field VSS_WS_FAILED_AT_PREPARE_BACKUP

The writer vetoed the shadow copy creation process during the backup preparation state.


### -field VSS_WS_FAILED_AT_PREPARE_SNAPSHOT

The writer vetoed the shadow copy creation process during the <a href="vssgloss_p.htm">PrepareForSnapshot</a> state.


### -field VSS_WS_FAILED_AT_FREEZE

The writer vetoed the shadow copy creation process during the freeze state.


### -field VSS_WS_FAILED_AT_THAW

The writer vetoed the shadow copy creation process during the thaw state.


### -field VSS_WS_FAILED_AT_POST_SNAPSHOT

The writer vetoed the shadow copy creation process during the 
     <a href="vssgloss_p.htm">PostSnapshot</a> state.


### -field VSS_WS_FAILED_AT_BACKUP_COMPLETE

The shadow copy has been created and the writer failed during the 
      <a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> state. A writer 
      should save information about this failure to the error log. For additional information on logging, see 
      <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.


### -field VSS_WS_FAILED_AT_PRE_RESTORE

The writer failed during the 
      <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> state.


### -field VSS_WS_FAILED_AT_POST_RESTORE

The writer failed during the 
      <a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> state.


### -field VSS_WS_FAILED_AT_BACKUPSHUTDOWN

The writer failed during the shutdown of the backup application.


### -field VSS_WS_COUNT

Reserved value.


## -remarks



A requester determines the state of a writer through 
    <a href="https://msdn.microsoft.com/652e9630-291d-41cd-96d9-6a63988932a5">IVssBackupComponents::GetWriterStatus</a>.




## -see-also




<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>



<a href="https://msdn.microsoft.com/652e9630-291d-41cd-96d9-6a63988932a5">IVssBackupComponents::GetWriterStatus</a>
 

 

