---
UID: NE:vss._VSS_WRITER_STATE
title: "_VSS_WRITER_STATE"
author: windows-driver-content
description: Indicates the current state of the writer.
old-location: base\vss_writer_state.htm
old-project: VSS
ms.assetid: 97aa20a3-4d58-49e8-83c0-fc33c700c410
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PVSS_WRITER_STATE, PVSS_WRITER_STATE, PVSS_WRITER_STATE enumeration pointer [VSS], VSS_WRITER_STATE, VSS_WRITER_STATE enumeration [VSS], VSS_WS_COUNT, VSS_WS_FAILED_AT_BACKUPSHUTDOWN, VSS_WS_FAILED_AT_BACKUP_COMPLETE, VSS_WS_FAILED_AT_FREEZE, VSS_WS_FAILED_AT_IDENTIFY, VSS_WS_FAILED_AT_POST_RESTORE, VSS_WS_FAILED_AT_POST_SNAPSHOT, VSS_WS_FAILED_AT_PREPARE_BACKUP, VSS_WS_FAILED_AT_PREPARE_SNAPSHOT, VSS_WS_FAILED_AT_PRE_RESTORE, VSS_WS_FAILED_AT_THAW, VSS_WS_STABLE, VSS_WS_UNKNOWN, VSS_WS_WAITING_FOR_BACKUP_COMPLETE, VSS_WS_WAITING_FOR_FREEZE, VSS_WS_WAITING_FOR_POST_SNAPSHOT, VSS_WS_WAITING_FOR_THAW, _VSS_WRITER_STATE, _win32_vss_writer_state, base.vss_writer_state, vss/PVSS_WRITER_STATE, vss/VSS_WRITER_STATE, vss/VSS_WS_COUNT, vss/VSS_WS_FAILED_AT_BACKUPSHUTDOWN, vss/VSS_WS_FAILED_AT_BACKUP_COMPLETE, vss/VSS_WS_FAILED_AT_FREEZE, vss/VSS_WS_FAILED_AT_IDENTIFY, vss/VSS_WS_FAILED_AT_POST_RESTORE, vss/VSS_WS_FAILED_AT_POST_SNAPSHOT, vss/VSS_WS_FAILED_AT_PREPARE_BACKUP, vss/VSS_WS_FAILED_AT_PREPARE_SNAPSHOT, vss/VSS_WS_FAILED_AT_PRE_RESTORE, vss/VSS_WS_FAILED_AT_THAW, vss/VSS_WS_STABLE, vss/VSS_WS_UNKNOWN, vss/VSS_WS_WAITING_FOR_BACKUP_COMPLETE, vss/VSS_WS_WAITING_FOR_FREEZE, vss/VSS_WS_WAITING_FOR_POST_SNAPSHOT, vss/VSS_WS_WAITING_FOR_THAW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: VSS_WRITER_STATE, *PVSS_WRITER_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vss.h
api_name:
-	VSS_WRITER_STATE
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

