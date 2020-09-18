---
UID: NS:bits._BG_JOB_TIMES
title: BG_JOB_TIMES (bits.h)
description: Provides job-related time stamps.
helpviewer_keywords: ["BG_JOB_TIMES","BG_JOB_TIMES structure [BITS]","_drz_bg_job_times","bits.bg_job_times","bits/BG_JOB_TIMES"]
old-location: bits\bg_job_times.htm
tech.root: Bits
ms.assetid: d7ee63f7-e2d1-451d-b200-cccb86816f21
ms.date: 12/05/2018
ms.keywords: BG_JOB_TIMES, BG_JOB_TIMES structure [BITS], _drz_bg_job_times, bits.bg_job_times, bits/BG_JOB_TIMES
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
req.typenames: BG_JOB_TIMES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BG_JOB_TIMES
 - bits/_BG_JOB_TIMES
 - BG_JOB_TIMES
 - bits/BG_JOB_TIMES
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
 - BG_JOB_TIMES
---

# BG_JOB_TIMES structure


## -description

Provides job-related time stamps.

## -struct-fields

### -field CreationTime

Time the job was created. The time is specified as 
<a href="/windows/win32/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field ModificationTime

Time the job was last modified or bytes were transferred. Adding files or calling any of the set methods in the 
<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyjob4">IBackgroundCopyJob*</a> interfaces changes this value. In addition, changes to the state of the job and calling the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-suspend">Suspend</a>, 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">Resume</a>, 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">Cancel</a>, and 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">Complete</a> methods change this value. The time is specified as 
<a href="/windows/win32/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field TransferCompletionTime

Time the job entered the BG_JOB_STATE_TRANSFERRED state. The time is specified as 
<a href="/windows/win32/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-gettimes">IBackgroundCopyJob::GetTimes</a>