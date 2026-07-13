---
UID: NE:bits.BG_JOB_PRIORITY
title: BG_JOB_PRIORITY (bits.h)
description: Defines constants that specify the priority level of a job.
helpviewer_keywords: ["BG_JOB_PRIORITY","BG_JOB_PRIORITY enumeration [BITS]","BG_JOB_PRIORITY_FOREGROUND","BG_JOB_PRIORITY_HIGH","BG_JOB_PRIORITY_LOW","BG_JOB_PRIORITY_NORMAL","_drz_bg_job_priority","bits.bg_job_priority","bits/BG_JOB_PRIORITY","bits/BG_JOB_PRIORITY_FOREGROUND","bits/BG_JOB_PRIORITY_HIGH","bits/BG_JOB_PRIORITY_LOW","bits/BG_JOB_PRIORITY_NORMAL"]
old-location: bits\bg_job_priority.htm
tech.root: Bits
ms.assetid: bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e
ms.date: 02/20/2019
ms.keywords: BG_JOB_PRIORITY, BG_JOB_PRIORITY enumeration [BITS], BG_JOB_PRIORITY_FOREGROUND, BG_JOB_PRIORITY_HIGH, BG_JOB_PRIORITY_LOW, BG_JOB_PRIORITY_NORMAL, _drz_bg_job_priority, bits.bg_job_priority, bits/BG_JOB_PRIORITY, bits/BG_JOB_PRIORITY_FOREGROUND, bits/BG_JOB_PRIORITY_HIGH, bits/BG_JOB_PRIORITY_LOW, bits/BG_JOB_PRIORITY_NORMAL
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
targetos: Windows
req.typenames: BG_JOB_PRIORITY
req.redist: 
f1_keywords:
 - BG_JOB_PRIORITY
 - bits/BG_JOB_PRIORITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits.h
api_name:
 - BG_JOB_PRIORITY
---

# BG_JOB_PRIORITY enumeration


## -description

Defines constants that specify the priority level of a job.

## -enum-fields

### -field BG_JOB_PRIORITY_FOREGROUND:0

Transfers the job in the foreground. Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience. This is the highest priority level.

### -field BG_JOB_PRIORITY_HIGH

Transfers the job in the background with a high priority. Background transfers use idle network bandwidth of the client to transfer files. This is the highest background priority level.

### -field BG_JOB_PRIORITY_NORMAL

Transfers the job in the background with a normal priority. Background transfers use idle network bandwidth of the client to transfer files. This is the default priority level.

### -field BG_JOB_PRIORITY_LOW

Transfers the job in the background with a low priority. Background transfers use idle network bandwidth of the client to transfer files. This is the lowest background priority level.

## -remarks

For a background job, the priority level determines when the job is processed relative to other jobs in the transfer queue. A higher-priority job preempts a lower-priority job. Jobs at the same priority level share transfer time, which prevents a large job from blocking the transfer queue. Lower-priority jobs don't receive transfer time until all higher-priority jobs are transferred, or are in an error state. 

Multiple foreground transfers can take place simultaneously. However, multiple files in the same job are transferred sequentially. For example, if you have 5 files that you would like to download concurrently, you may consider creating 5 foreground jobs, one for each transfer.

**BITS 1.5 and earlier:** BITS processes one job at a time. Foreground jobs have the highest priority and run before background jobs.

For more information, see [Best practices when using BITS](/windows/desktop/bits/best-practices-when-using-bits).

## -see-also

* [IBackgroundCopyJob::GetPriority method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getpriority)
* [IBackgroundCopyJob::SetPriority method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setpriority)

