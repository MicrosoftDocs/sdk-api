---
UID: NS:bits1_5._BG_JOB_REPLY_PROGRESS
title: "_BG_JOB_REPLY_PROGRESS"
author: windows-sdk-content
description: The BG_JOB_REPLY_PROGRESS structure provides progress information related to the reply portion of an upload-reply job.
old-location: bits\bg_job_reply_progress.htm
tech.root: bits
ms.assetid: ea78ee22-87b2-4859-bd49-dd309c8aa234
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: BG_JOB_REPLY_PROGRESS, BG_JOB_REPLY_PROGRESS structure [BITS], _BG_JOB_REPLY_PROGRESS, _drz_bg_job_reply_progress, bits.bg_job_reply_progress, bits1_5/BG_JOB_REPLY_PROGRESS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
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
 - Bits1_5.h
api_name:
 - BG_JOB_REPLY_PROGRESS
product: Windows
targetos: Windows
req.typenames: BG_JOB_REPLY_PROGRESS
req.redist: BITS 1.5 on  Windows XP
---

# _BG_JOB_REPLY_PROGRESS structure


## -description


The 
<b>BG_JOB_REPLY_PROGRESS</b> structure provides progress information related to the reply portion of an upload-reply job.


## -struct-fields




### -field BytesTotal

Size of the file in bytes. The value is <b>BG_SIZE_UNKNOWN</b> if the reply has not begun.


### -field BytesTransferred

Number of bytes transferred.


## -see-also




<a href="https://msdn.microsoft.com/76509b1a-fdfb-4236-8554-f63282bfc1b6">IBackgroundCopyJob2::GetReplyProgress</a>
 

 

