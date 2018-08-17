---
UID: NS:bits._BG_JOB_PROGRESS
title: "_BG_JOB_PROGRESS"
author: windows-sdk-content
description: The BG_JOB_PROGRESS structure provides job-related progress information, such as the number of bytes and files transferred.
old-location: bits\bg_job_progress.htm
old-project: bits
ms.assetid: 92c5d1d6-1e0b-4b92-9dc5-ec9a4e2c4649
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BG_JOB_PROGRESS, BG_JOB_PROGRESS structure [BITS], _BG_JOB_PROGRESS, _drz_bg_job_progress, bits.bg_job_progress, bits/BG_JOB_PROGRESS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bits.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_PROGRESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits.h
api_name:
 - BG_JOB_PROGRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BG_JOB_PROGRESS structure


## -description


The 
<b>BG_JOB_PROGRESS</b> structure provides job-related progress information, such as the number of bytes and files transferred. For upload jobs, the progress applies to the upload file, not the reply file. To view reply file progress, see the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362808(v=VS.85).aspx">BG_JOB_REPLY_PROGRESS</a> structure.


## -struct-fields




### -field BytesTotal

Total number of bytes to transfer for all files in the job. If the value is BG_SIZE_UNKNOWN, the total size of all files in the job has not been determined. BITS does not set this value if it cannot determine the size of one of the files. For example, if the specified file or server does not exist, BITS cannot determine the size of the file.

If you are downloading ranges from the file, <b>BytesTotal</b> includes the total number of bytes you want to download from the file.


### -field BytesTransferred

Number of bytes transferred.


### -field FilesTotal

Total number of files to transfer for this job.


### -field FilesTransferred

Number of files transferred.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362801(v=VS.85).aspx">BG_FILE_PROGRESS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362808(v=VS.85).aspx">BG_JOB_REPLY_PROGRESS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362991(v=VS.85).aspx">IBackgroundCopyJob3::AddFileWithRanges</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363034(v=VS.85).aspx">IBackgroundCopyJob::GetProgress</a>
 

 

