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

# VSS_FILE_RESTORE_STATUS enumeration


## -description


The <b>VSS_FILE_RESTORE_STATUS</b> enumeration 
    defines the set of statuses of a file restore operation performed on the files managed by a 
    selected component or component set (see 
    <a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability and 
    Logical Paths</a> for information on selecting components).


## -enum-fields




### -field VSS_RS_UNDEFINED

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
    <a href="https://msdn.microsoft.com/669d61cc-c586-4dcc-a936-5343a393d371">IVssBackupComponents::SetFileRestoreStatus</a>) 
    for every component (and its component set, if it defines one) explicitly added for restore to the Backup 
    Components Document (using either 
    <a href="https://msdn.microsoft.com/8f8051d3-b1b6-418b-8a53-0ddc82a20bb3">IVssBackupComponents::SetSelectedForRestore</a> or 
    <a href="https://msdn.microsoft.com/8eea27d7-6780-49cf-97ea-8876a9a2c8f8">IVssBackupComponents::AddRestoreSubcomponent</a>).

Writers and requesters can query the status of the restoration of a component or a component set defined by a 
    selectable component with calls to 
    <a href="https://msdn.microsoft.com/b79c4443-c850-4edf-bdd2-917e22e67d77">IVssComponent::GetFileRestoreStatus</a>. If
    this method is called for a component that was not selected, the value returned is undefined.




## -see-also




<a href="https://msdn.microsoft.com/669d61cc-c586-4dcc-a936-5343a393d371">IVssBackupComponents::SetFileRestoreStatus</a>



<a href="https://msdn.microsoft.com/b79c4443-c850-4edf-bdd2-917e22e67d77">IVssComponent::GetFileRestoreStatus</a>
 

 

