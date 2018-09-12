---
UID: NE:bits.__MIDL_IBackgroundCopyJob_0001
title: "__MIDL_IBackgroundCopyJob_0001"
author: windows-sdk-content
description: The BG_JOB_PRIORITY enumeration defines the constant values that specify the priority level of a job.
old-location: bits\bg_job_priority.htm
tech.root: bits
ms.assetid: bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BG_JOB_PRIORITY, BG_JOB_PRIORITY enumeration [BITS], BG_JOB_PRIORITY_FOREGROUND, BG_JOB_PRIORITY_HIGH, BG_JOB_PRIORITY_LOW, BG_JOB_PRIORITY_NORMAL, __MIDL_IBackgroundCopyJob_0001, _drz_bg_job_priority, bits.bg_job_priority, bits/BG_JOB_PRIORITY, bits/BG_JOB_PRIORITY_FOREGROUND, bits/BG_JOB_PRIORITY_HIGH, bits/BG_JOB_PRIORITY_LOW, bits/BG_JOB_PRIORITY_NORMAL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
 - Bits.h
api_name:
 - BG_JOB_PRIORITY
product: Windows
targetos: Windows
req.typenames: BG_JOB_PRIORITY
req.redist: 
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

For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa362783(v=VS.85).aspx">Best Practices When Using BITS</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa363033(v=VS.85).aspx">IBackgroundCopyJob::GetPriority</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363046(v=VS.85).aspx">IBackgroundCopyJob::SetPriority</a>
 

 

