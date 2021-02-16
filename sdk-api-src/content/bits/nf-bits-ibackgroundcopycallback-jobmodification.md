---
UID: NF:bits.IBackgroundCopyCallback.JobModification
title: IBackgroundCopyCallback::JobModification (bits.h)
description: BITS calls your implementation of the JobModification method when the job has been modified.
helpviewer_keywords: ["IBackgroundCopyCallback interface [BITS]","JobModification method","IBackgroundCopyCallback.JobModification","IBackgroundCopyCallback::JobModification","JobModification","JobModification method [BITS]","JobModification method [BITS]","IBackgroundCopyCallback interface","_drz_ibackgroundcopycallback_jobmodification","bits.ibackgroundcopycallback_jobmodification","bits/IBackgroundCopyCallback::JobModification"]
old-location: bits\ibackgroundcopycallback_jobmodification.htm
tech.root: Bits
ms.assetid: 7614756d-92d1-4b71-a589-c0e39728a51c
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyCallback interface [BITS],JobModification method, IBackgroundCopyCallback.JobModification, IBackgroundCopyCallback::JobModification, JobModification, JobModification method [BITS], JobModification method [BITS],IBackgroundCopyCallback interface, _drz_ibackgroundcopycallback_jobmodification, bits.ibackgroundcopycallback_jobmodification, bits/IBackgroundCopyCallback::JobModification
req.header: bits.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyCallback::JobModification
 - bits/IBackgroundCopyCallback::JobModification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.h
api_name:
 - IBackgroundCopyCallback.JobModification
---

# IBackgroundCopyCallback::JobModification


## -description

BITS calls your implementation of the 
<b>JobModification</b> method when the job has been modified. The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.

## -parameters

### -param pJob [in]

Contains the methods for accessing property, progress, and state information of the job. Do not release <i>pJob</i>; BITS releases the interface when the <b>JobModification</b> method returns.

### -param dwReserved [in]

Reserved for future use.

## -returns

This method should return <b>S_OK</b>.

## -remarks

Your implementation may not receive all modification events under maximum resource load conditions.

BITS generates a high volume of modification events; consider creating a timer and polling for state and progress information or limiting your use of this callback. If you use this callback, keep your implementation short.

BITS does not generate a modify event when the state of the job changes to BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSFERRED.

<div class="alert"><b>Note</b>  BITS supports up to four simultaneous notifications per user. If one or more applications  block all four notifications for a user from returning, an application running as the same user will not receive  notifications until one or more of the blocking notifications return. </div>
<div> </div>

#### Examples

See the example code for the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>