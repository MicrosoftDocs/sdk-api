---
UID: NS:bits._BG_JOB_PROGRESS
title: BG_JOB_PROGRESS (bits.h)
description: Provides job-related progress information, such as the number of bytes and files transferred.
helpviewer_keywords: ["BG_JOB_PROGRESS","BG_JOB_PROGRESS structure [BITS]","_drz_bg_job_progress","bits.bg_job_progress","bits/BG_JOB_PROGRESS"]
old-location: bits\bg_job_progress.htm
tech.root: Bits
ms.assetid: 92c5d1d6-1e0b-4b92-9dc5-ec9a4e2c4649
ms.date: 12/05/2018
ms.keywords: BG_JOB_PROGRESS, BG_JOB_PROGRESS structure [BITS], _drz_bg_job_progress, bits.bg_job_progress, bits/BG_JOB_PROGRESS
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
req.typenames: BG_JOB_PROGRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BG_JOB_PROGRESS
 - bits/_BG_JOB_PROGRESS
 - BG_JOB_PROGRESS
 - bits/BG_JOB_PROGRESS
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
 - BG_JOB_PROGRESS
---

## -description

Provides job-related progress information, such as the number of bytes and files transferred. For upload jobs, the progress applies to the upload file, not the reply file. To view reply file progress, see the 
<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_job_reply_progress">BG_JOB_REPLY_PROGRESS</a> structure.

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

<a href="/windows/desktop/api/bits/ns-bits-bg_file_progress">BG_FILE_PROGRESS</a>



<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_job_reply_progress">BG_JOB_REPLY_PROGRESS</a>



<a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges">IBackgroundCopyJob3::AddFileWithRanges</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getprogress">IBackgroundCopyJob::GetProgress</a>