---
UID: NF:bits3_0.IBackgroundCopyJob4.SetMaximumDownloadTime
title: IBackgroundCopyJob4::SetMaximumDownloadTime (bits3_0.h)
description: Sets the maximum time that BITS will spend transferring the files in the job.
helpviewer_keywords: ["IBackgroundCopyJob4 interface [BITS]","SetMaximumDownloadTime method","IBackgroundCopyJob4.SetMaximumDownloadTime","IBackgroundCopyJob4::SetMaximumDownloadTime","SetMaximumDownloadTime","SetMaximumDownloadTime method [BITS]","SetMaximumDownloadTime method [BITS]","IBackgroundCopyJob4 interface","bits.ibackgroundcopyjob4_setmaximumdownloadtime","bits3_0/IBackgroundCopyJob4::SetMaximumDownloadTime"]
old-location: bits\ibackgroundcopyjob4_setmaximumdownloadtime.htm
tech.root: Bits
ms.assetid: 9e29c082-5bd1-465a-8853-aea81a593db6
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob4 interface [BITS],SetMaximumDownloadTime method, IBackgroundCopyJob4.SetMaximumDownloadTime, IBackgroundCopyJob4::SetMaximumDownloadTime, SetMaximumDownloadTime, SetMaximumDownloadTime method [BITS], SetMaximumDownloadTime method [BITS],IBackgroundCopyJob4 interface, bits.ibackgroundcopyjob4_setmaximumdownloadtime, bits3_0/IBackgroundCopyJob4::SetMaximumDownloadTime
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob4::SetMaximumDownloadTime
 - bits3_0/IBackgroundCopyJob4::SetMaximumDownloadTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJob4.SetMaximumDownloadTime
---

# IBackgroundCopyJob4::SetMaximumDownloadTime


## -description

Sets the maximum time that BITS will spend transferring the files in the job.

## -parameters

### -param Timeout [in]

Maximum time, in seconds, that BITS will spend transferring the files in the job. The default is 7,776,000 seconds (90 days).

## -returns

The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

The value is the maximum elapsed time that the job can spend in the CONNECTING or TRANSFERRING state. Time spent in the QUEUED or TRANSIENT_ERROR state does not count against the timeout value. The job enters the fatal error state with an error code of BG_E_MAXDOWNLOAD_TIMEOUT if the transfer time exceeds the timeout value. 

Note that if the computer sleeps while BITS is transferring the job's data, the time spent sleeping will count against the timeout even though data is not being transferred.

Calling the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a> method, resets the elapsed time.

This method overrides the MaxDownloadTime group policy.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyjob4">IBackgroundCopyJob4</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-getmaximumdownloadtime">IBackgroundCopyJob4::GetMaximumDownloadTime</a>