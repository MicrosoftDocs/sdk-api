---
UID: NS:bits._BG_JOB_TIMES
title: "_BG_JOB_TIMES"
author: windows-sdk-content
description: The BG_JOB_TIMES structure provides job-related time stamps.
old-location: bits\bg_job_times.htm
tech.root: bits
ms.assetid: d7ee63f7-e2d1-451d-b200-cccb86816f21
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: BG_JOB_TIMES, BG_JOB_TIMES structure [BITS], _BG_JOB_TIMES, _drz_bg_job_times, bits.bg_job_times, bits/BG_JOB_TIMES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - BG_JOB_TIMES
product: Windows
targetos: Windows
req.typenames: BG_JOB_TIMES
req.redist: 
---

# _BG_JOB_TIMES structure


## -description


The 
<b>BG_JOB_TIMES</b> structure provides job-related time stamps.


## -struct-fields




### -field CreationTime

Time the job was created. The time is specified as 
<a href="http://go.microsoft.com/fwlink/p/?linkid=128776">FILETIME</a>.


### -field ModificationTime

Time the job was last modified or bytes were transferred. Adding files or calling any of the set methods in the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362995(v=VS.85).aspx">IBackgroundCopyJob*</a> interfaces changes this value. In addition, changes to the state of the job and calling the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363048(v=VS.85).aspx">Suspend</a>, 
<a href="https://msdn.microsoft.com/en-us/library/Aa363039(v=VS.85).aspx">Resume</a>, 
<a href="https://msdn.microsoft.com/en-us/library/Aa363020(v=VS.85).aspx">Cancel</a>, and 
<a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">Complete</a> methods change this value. The time is specified as 
<a href="http://go.microsoft.com/fwlink/p/?linkid=128776">FILETIME</a>.


### -field TransferCompletionTime

Time the job entered the BG_JOB_STATE_TRANSFERRED state. The time is specified as 
<a href="http://go.microsoft.com/fwlink/p/?linkid=128776">FILETIME</a>.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa363037(v=VS.85).aspx">IBackgroundCopyJob::GetTimes</a>
 

 

