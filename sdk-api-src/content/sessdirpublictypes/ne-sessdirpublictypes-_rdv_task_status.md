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

# _RDV_TASK_STATUS enumeration


## -description


Used with the <a href="https://msdn.microsoft.com/3021ea7a-2627-48d1-8df5-c40e7a9b51c5">IRDVTaskPluginNotifySink::OnTaskStateChange</a> method to indicate the status of a task.


## -enum-fields




### -field RDV_TASK_STATUS_UNKNOWN

The task state cannot be determined.


### -field RDV_TASK_STATUS_SEARCHING

Searching for applicable tasks.


### -field RDV_TASK_STATUS_DOWNLOADING

Downloading tasks.


### -field RDV_TASK_STATUS_APPLYING

Performing tasks.


### -field RDV_TASK_STATUS_REBOOTING

Rebooting. The task may or may not be complete.


### -field RDV_TASK_STATUS_REBOOTED

Reboot completed. The task may or may not be complete.


### -field RDV_TASK_STATUS_SUCCESS

Task completed successfully.


### -field RDV_TASK_STATUS_FAILED

Task failed.


### -field RDV_TASK_STATUS_TIMEOUT

Task did not finish in the allotted time.


## -see-also




<a href="https://msdn.microsoft.com/3021ea7a-2627-48d1-8df5-c40e7a9b51c5">IRDVTaskPluginNotifySink::OnTaskStateChange</a>
 

 

