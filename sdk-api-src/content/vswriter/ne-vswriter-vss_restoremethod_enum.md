---
UID: NE:vswriter.VSS_RESTOREMETHOD_ENUM
title: VSS_RESTOREMETHOD_ENUM
author: windows-sdk-content
description: Used by a writer at backup time to specify through its Writer Metadata Document the default file restore method.
old-location: base\vss_restoremethod_enum.htm
tech.root: VSS
ms.assetid: 4c6be981-4271-4040-8f6e-725616355062
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VSS_RESTOREMETHOD_ENUM, VSS_RESTOREMETHOD_ENUM enumeration [VSS], VSS_RME_CUSTOM, VSS_RME_RESTORE_AT_REBOOT, VSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE, VSS_RME_RESTORE_IF_CAN_REPLACE, VSS_RME_RESTORE_IF_NOT_THERE, VSS_RME_RESTORE_STOP_START, VSS_RME_RESTORE_TO_ALTERNATE_LOCATION, VSS_RME_STOP_RESTORE_START, VSS_RME_UNDEFINED, _win32_vss_restoremethod_enum, base.vss_restoremethod_enum, enumeration [VSS], vswriter/VSS_RESTOREMETHOD_ENUM, vswriter/VSS_RME_CUSTOM, vswriter/VSS_RME_RESTORE_AT_REBOOT, vswriter/VSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE, vswriter/VSS_RME_RESTORE_IF_CAN_REPLACE, vswriter/VSS_RME_RESTORE_IF_NOT_THERE, vswriter/VSS_RME_RESTORE_STOP_START, vswriter/VSS_RME_RESTORE_TO_ALTERNATE_LOCATION, vswriter/VSS_RME_STOP_RESTORE_START, vswriter/VSS_RME_UNDEFINED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_RESTOREMETHOD_ENUM
product: Windows
targetos: Windows
req.typenames: VSS_RESTOREMETHOD_ENUM
req.redist: 
---

# VSS_RESTOREMETHOD_ENUM enumeration


## -description


The <b>VSS_RESTOREMETHOD_ENUM</b> enumeration is 
    used by a writer at backup time to specify through its Writer Metadata Document the default file restore 
    method to be used with all the files in all the components it manages.

The restore method is writer-wide and is also referred to as the original restore target and indicated by a 
    <a href="https://msdn.microsoft.com/85b154c0-ebe8-4c17-8cab-0f886bf070e2">VSS_RESTORE_TARGET</a> value of 
    <b>VSS_RT_ORIGINAL</b>.


## -enum-fields




### -field VSS_RME_UNDEFINED

No restore method is defined. 
      

This indicates an error on the part of the writer.

This value is not supported for express writers.


### -field VSS_RME_RESTORE_IF_NOT_THERE

The requester should restore the files of a selected component or component set only if there are no versions of 
      those files currently on the disk. 
      

Unless alternate location mappings are defined for file restoration, if a version of any file managed by a 
       selected component or component set is currently on the disk, none of the files managed by the selected 
       component or component set should be restored.

If a file's alternate location mapping is defined, and a version of the files is present on disk at the 
       original location, files should be written to the alternate location only if no version of the file exists at 
       the alternate location.


### -field VSS_RME_RESTORE_IF_CAN_REPLACE

The requester should restore files of a selected component or component set only if the files currently on the disk can be overwritten. 
      

Unless alternate location mappings are defined for file restoration, if there is a version of any file that 
       cannot be overwritten of the selected component or component set on the disk, none of the files managed by the 
       component or component set should be restored.

If a file's alternate location mapping is defined, files should be written to the alternate location.


### -field VSS_RME_STOP_RESTORE_START

The requester should perform the restore operation as follows:

<ol>
<li>Send the <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event and wait for all writers to process it.</li>
<li>Stop the service.</li>
<li>Restore the files to their original locations.</li>
<li>Restart the service.</li>
<li>Send the <a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event and wait for all writers to process it.</li>
</ol>
The service to be stopped is specified the writer beforehand when it calls the <a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">IVssCreateWriterMetadata::SetRestoreMethod</a> method. The requester can obtain the name of the service by calling the <a href="https://msdn.microsoft.com/c93f841f-057c-4aee-b8f2-263395e84c7b">IVssExamineWriterMetadata::GetRestoreMethod</a> method.

Note that if the writer is hosted in the service that is being stopped, that writer will not receive the <a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event, because the writer instance ID changes when the service is stopped and restarted.


### -field VSS_RME_RESTORE_TO_ALTERNATE_LOCATION

The requester should restore the files of the selected component or component set to the location specified by the 
      alternate location mapping specified in the writer component metadata file. (See 
      <a href="https://msdn.microsoft.com/966c40d4-8c19-43cc-ba49-028763478f49">IVssCreateWriterMetadata::AddAlternateLocationMapping</a>, 
      <a href="https://msdn.microsoft.com/8c6537eb-67ba-4d6a-ac86-44da176ef5c5">IVssComponent::GetAlternateLocationMapping</a>, 
      <a href="https://msdn.microsoft.com/1264d4bc-dd45-41e7-9f95-c6e9aebd4d22">IVssExamineWriterMetadata::GetAlternateLocationMapping</a>, 
      and <a href="https://msdn.microsoft.com/3bb787eb-ac15-40d0-9901-b869442399c5">IVssWMFiledesc::GetAlternateLocation</a>.)

This value is not supported for express writers.


### -field VSS_RME_RESTORE_AT_REBOOT

The requester should restore the files of a selected component or component set after the computer is restarted. 
      

The files to be restored should be copied to a temporary location, and the requester should use 
       <a href="https://msdn.microsoft.com/5fb4f897-66ed-49d7-913a-fb6e7cecdfa3">MoveFileEx</a> with the 
       <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> flag to complete the restoration of these files to their 
       proper location after the computer is restarted.


### -field VSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE

If possible, the requester should restore the files of the selected component or component set to their correct 
      location immediately. 
      

If there are versions of any of the files managed by the selected component or component set on the disk that 
       cannot be overwritten, then all the files managed by the selected component or component set should be restored 
       after the computer is restarted.

In this case, files to be restored should be copied to a temporary location on disk, and the requester should 
       use <a href="https://msdn.microsoft.com/5fb4f897-66ed-49d7-913a-fb6e7cecdfa3">MoveFileEx</a> with the 
       <b>MOVEFILE_DELAY_UNTIL_REBOOT</b> flag to complete the restoration of these files to their 
       proper location after the computer is restarted.


### -field VSS_RME_CUSTOM

The requester should use a custom restore method to restore the files that are managed by the selected 
      component or component set. 
      

A custom restore may use file retrieval API functions or protocols that are private to a given writer 
       application. Such a restore need not use the information in the writer component metadata file. (See 
       <a href="https://msdn.microsoft.com/6aaa9220-8aa4-4ddc-9ae0-d7aa05a96fa7">Custom Backups and Restores</a> for more 
       information.)

This value is not supported for express writers.


### -field VSS_RME_RESTORE_STOP_START

The requester should perform the restore operation as follows:

<ol>
<li>Send the <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event and wait for all writers to process it.</li>
<li>Restore the files to their original locations.</li>
<li>Send the <a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event and wait for all writers to process it.</li>
<li>Stop the service.</li>
<li>Restart the service.</li>
</ol>
The service to be stopped is specified by the writer beforehand when it calls the <a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">IVssCreateWriterMetadata::SetRestoreMethod</a> method. The requester can obtain the name of the service by calling the <a href="https://msdn.microsoft.com/c93f841f-057c-4aee-b8f2-263395e84c7b">IVssExamineWriterMetadata::GetRestoreMethod</a> method.


## -remarks



A writer sets the restore method in the Writer Metadata Document by calling 
    <a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">IVssCreateWriterMetadata::SetRestoreMethod</a> 
    during backup to specify its desired restore method in its metadata.

A requester retrieves a writer's requested restore method by calling 
    <a href="https://msdn.microsoft.com/c93f841f-057c-4aee-b8f2-263395e84c7b">IVssExamineWriterMetadata::GetRestoreMethod</a> 
    and acts accordingly.

The restore method applies to all files in all components of a given writer.

The restore method may be overridden on a component-by-component basis at restore time if a writer sets a 
    <a href="https://msdn.microsoft.com/85b154c0-ebe8-4c17-8cab-0f886bf070e2">VSS_RESTORE_TARGET</a> value other than
    <b>VSS_RT_ORIGINAL</b> with 
    <a href="https://msdn.microsoft.com/6e8b9322-6611-4a47-aa7a-876be01d33b8">IVssComponent::SetRestoreTarget</a>.

A restore method of <b>VSS_RME_RESTORE_TO_ALTERNATE_LOCATION</b> without an alternate 
    location mapping defined constitutes a writer error, and the requester should report it as such.

When a restore method requires a check on the status of files currently on disk 
    (<b>VSS_RME_RESTORE_IF_NOT_THERE</b>, 
    <b>VSS_RME_RESTORE_IF_CAN_REPLACE</b>, or 
    <b>VSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE</b>), ideally, you should use file I/O 
    operations to verify that an entire component can be restored before actually proceeding with the restore.

The safest way to do this would be to open exclusively (no-sharing) all the target files with 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> prior to the restore.

In the case of <b>VSS_RME_RESTORE_IF_NOT_THERE</b>, a creation disposition flag of 
    <b>CREATE_NEW</b> should also be set.

If the open operations succeed, the restore can proceed and should use the handles returned by 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> to actually write restored data to disk.

If not, an error can be returned—depending on the method—or 
    alternate location mapping checked and (if it is available) used, or the components files staged for restore at 
    the next reboot.

This may be a problem for very large components (some of which may have thousands of files), due to system 
    overhead.

In this case, an available though less reliable option is to do the following:

<ol>
<li>Copy all files currently on disk and to be restored to a temporary cache.</li>
<li>Attempt to replace the files currently on disk with the backed-up files (which could be either on disk in a 
      second temporary area, or on a backup medium).</li>
<li>If any files fail to restore, then terminate the restore operation and copy the original files back from 
      their temporary location and proceed with alternate location mapping or restore on reboot operations.</li>
</ol>
For more information on backup and restore file locations under VSS, see 
    <a href="https://msdn.microsoft.com/7609c392-d5f8-48c2-8e7e-f35f56cf94f8">Non-Default Backup And Restore 
    Locations</a>.




## -see-also




<a href="https://msdn.microsoft.com/349ec124-f3f5-4142-8600-8d9f508c9bb2">IVssBackupComponents::AddAlternativeLocationMapping</a>



<a href="https://msdn.microsoft.com/8c6537eb-67ba-4d6a-ac86-44da176ef5c5">IVssComponent::GetAlternateLocationMapping</a>



<a href="https://msdn.microsoft.com/966c40d4-8c19-43cc-ba49-028763478f49">IVssCreateWriterMetadata::AddAlternateLocationMapping</a>



<a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">IVssCreateWriterMetadata::SetRestoreMethod</a>



<a href="https://msdn.microsoft.com/1264d4bc-dd45-41e7-9f95-c6e9aebd4d22">IVssExamineWriterMetadata::GetAlternateLocationMapping</a>



<a href="https://msdn.microsoft.com/c93f841f-057c-4aee-b8f2-263395e84c7b">IVssExamineWriterMetadata::GetRestoreMethod</a>



<a href="https://msdn.microsoft.com/3bb787eb-ac15-40d0-9901-b869442399c5">IVssWMFiledesc::GetAlternateLocation</a>



<a href="https://msdn.microsoft.com/a3e45d52-4d9a-4bdf-a8e5-622939be6f2c">VSS_WRITERRESTORE_ENUM</a>
 

 

