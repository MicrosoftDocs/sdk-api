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

# __MIDL_IBackgroundCopyJob_0001 enumeration


## -description


The 
<b>BG_JOB_PRIORITY</b> enumeration defines the constant values that specify the priority level of a job. 


## -enum-fields




### -field BG_JOB_PRIORITY_FOREGROUND

Transfers the job in the foreground. Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience. This is the highest priority level.


### -field BG_JOB_PRIORITY_HIGH

Transfers the job in the background with a high priority. Background transfers use idle network bandwidth of the client to transfer files. This is the highest background priority level.


### -field BG_JOB_PRIORITY_NORMAL

Transfers the job in the background with a normal priority. Background transfers use idle network bandwidth of the client to transfer files. This is the default priority level.


### -field BG_JOB_PRIORITY_LOW

Transfers the job in the background with a low priority. Background transfers use idle network bandwidth of the client to transfer files. This is the lowest background priority level.


## -remarks



For background jobs, the priority level determines when the job is processed relative to other jobs in the transfer queue. Higher priority jobs preempt lower priority jobs. Jobs at the same priority level share transfer time, which prevents a large job from blocking the transfer queue. Lower priority jobs do not receive transfer time until all higher priority jobs are transferred or in an error state. 

Multiple foreground transfers can take place simultaneously. However, multiple files in the same job are transferred sequentially. For example, if you have 5 files that you would like to download concurrently, you may consider creating 5 foreground jobs, one for each transfer.

<b>BITS 1.5 and earlier:  </b>BITS processes one job at a time. Foreground jobs have the highest priority and run before background jobs.

For more information, see <a href="https://msdn.microsoft.com/f4a09a80-2a85-4b59-b0fd-c23c128973f7">Best Practices When Using BITS</a>.




## -see-also




<a href="https://msdn.microsoft.com/8602ed59-a372-4cb3-bbda-cf1c7afc3669">IBackgroundCopyJob::GetPriority</a>



<a href="https://msdn.microsoft.com/8b59128d-7e63-45dc-af0f-54ea844dac98">IBackgroundCopyJob::SetPriority</a>
 

 

