---
UID: NS:bits1_5._BG_JOB_REPLY_PROGRESS
title: BG_JOB_REPLY_PROGRESS
description: Provides progress information related to the reply portion of an upload-reply job.
helpviewer_keywords: ["BG_JOB_REPLY_PROGRESS","BG_JOB_REPLY_PROGRESS structure [BITS]","_drz_bg_job_reply_progress","bits.bg_job_reply_progress","bits1_5/BG_JOB_REPLY_PROGRESS"]
old-location: bits\bg_job_reply_progress.htm
tech.root: Bits
ms.assetid: ea78ee22-87b2-4859-bd49-dd309c8aa234
ms.date: 12/05/2018
ms.keywords: BG_JOB_REPLY_PROGRESS, BG_JOB_REPLY_PROGRESS structure [BITS], _drz_bg_job_reply_progress, bits.bg_job_reply_progress, bits1_5/BG_JOB_REPLY_PROGRESS
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
targetos: Windows
req.typenames: BG_JOB_REPLY_PROGRESS
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
f1_keywords:
 - _BG_JOB_REPLY_PROGRESS
 - bits1_5/_BG_JOB_REPLY_PROGRESS
 - BG_JOB_REPLY_PROGRESS
 - bits1_5/BG_JOB_REPLY_PROGRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits1_5.h
api_name:
 - BG_JOB_REPLY_PROGRESS
---

# BG_JOB_REPLY_PROGRESS structure


## -description

Provides progress information related to the reply portion of an upload-reply job.

## -struct-fields

### -field BytesTotal

Size of the file in bytes. The value is <b>BG_SIZE_UNKNOWN</b> if the reply has not begun.

### -field BytesTransferred

Number of bytes transferred.

## -see-also

<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress">IBackgroundCopyJob2::GetReplyProgress</a>