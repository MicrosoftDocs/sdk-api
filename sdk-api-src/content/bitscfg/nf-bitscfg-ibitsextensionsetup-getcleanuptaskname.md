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

# IBITSExtensionSetup::GetCleanupTaskName


## -description


Use the 
<b>GetCleanupTaskName</b> method to retrieve the name of the cleanup task associated with the virtual directory.


## -parameters




### -param pTaskName [out]

Null-terminated string containing the name of the cleanup task associated with the virtual directory. If <b>NULL</b>, BITS has not created a cleanup task for the virtual directory. When done, call the <b>SysFreeString</b> function to free <i>pTaskName</i>.


## -returns



This method returns <b>S_OK</b> for success. Otherwise, the method returns <b>S_FALSE</b> if a task name has not been specified for the virtual directory.




## -remarks



When you create a virtual directory and 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">enable</a> it for BITS uploads, BITS adds a work item in the 
<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>. The work item cleans up the virtual directory once every 12 hours by deleting jobs that have not been modified within the time-out period. To specify the time-out period, set the 
<a href="https://msdn.microsoft.com/08a40cc1-ec6d-4b65-971a-15c7b06df148">BITSSessionTimeout</a> IIS extension property.

Use the <i>pTaskName</i> name as an input parameter to the Schtasks.exe executable file, which you can use to change the properties of the cleanup task from a script.




## -see-also




<a href="https://msdn.microsoft.com/5b68dea2-f9a7-4a99-93d3-62c4f24b769f">IBITSExtensionSetup::EnableBITSUploads</a>



<a href="https://msdn.microsoft.com/ffa89d5b-7ba1-433b-a93d-032012906258">IBITSExtensionSetup::GetCleanupTask</a>
 

 

