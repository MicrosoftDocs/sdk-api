---
UID: NS:bits._BG_JOB_PROGRESS
title: BG_JOB_PROGRESS
author: windows-sdk-content
description: The BG_JOB_PROGRESS structure provides job-related progress information, such as the number of bytes and files transferred.
old-location: bits\bg_job_progress.htm
tech.root: bits
ms.assetid: 92c5d1d6-1e0b-4b92-9dc5-ec9a4e2c4649
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BG_JOB_PROGRESS, BG_JOB_PROGRESS structure [BITS], _drz_bg_job_progress, bits.bg_job_progress, bits/BG_JOB_PROGRESS
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
 - BG_JOB_PROGRESS
product: Windows
targetos: Windows
req.typenames: BG_JOB_PROGRESS
req.redist: 
---

# BG_JOB_PROGRESS structure


## -description


The 
<b>BG_JOB_PROGRESS</b> structure provides job-related progress information, such as the number of bytes and files transferred. For upload jobs, the progress applies to the upload file, not the reply file. To view reply file progress, see the 
<a href="https://msdn.microsoft.com/ea78ee22-87b2-4859-bd49-dd309c8aa234">BG_JOB_REPLY_PROGRESS</a> structure.


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




<a href="https://msdn.microsoft.com/322363b4-081e-4100-9087-e34c21a3ffae">BG_FILE_PROGRESS</a>



<a href="https://msdn.microsoft.com/ea78ee22-87b2-4859-bd49-dd309c8aa234">BG_JOB_REPLY_PROGRESS</a>



<a href="https://msdn.microsoft.com/b3601f23-1a69-47db-8943-7515652cf015">IBackgroundCopyJob3::AddFileWithRanges</a>



<a href="https://msdn.microsoft.com/30aae990-1cc1-468b-9e5f-7ef5ce6eeb9a">IBackgroundCopyJob::GetProgress</a>
 

 

