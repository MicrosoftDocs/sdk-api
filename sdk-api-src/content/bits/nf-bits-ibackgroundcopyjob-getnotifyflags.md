---
UID: NF:bits.IBackgroundCopyJob.GetNotifyFlags
title: IBackgroundCopyJob::GetNotifyFlags (bits.h)
description: Retrieves the event notification flags for the job.
helpviewer_keywords: ["BG_NOTIFY_DISABLE","BG_NOTIFY_JOB_ERROR","BG_NOTIFY_JOB_MODIFICATION","BG_NOTIFY_JOB_TRANSFERRED","GetNotifyFlags","GetNotifyFlags method [BITS]","GetNotifyFlags method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetNotifyFlags method","IBackgroundCopyJob.GetNotifyFlags","IBackgroundCopyJob::GetNotifyFlags","_drz_ibackgroundcopyjob_getnotifyflags","bits.ibackgroundcopyjob_getnotifyflags","bits/IBackgroundCopyJob::GetNotifyFlags"]
old-location: bits\ibackgroundcopyjob_getnotifyflags.htm
tech.root: Bits
ms.assetid: a4407816-a4c5-4734-9686-46d5a8133c2f
ms.date: 12/05/2018
ms.keywords: BG_NOTIFY_DISABLE, BG_NOTIFY_JOB_ERROR, BG_NOTIFY_JOB_MODIFICATION, BG_NOTIFY_JOB_TRANSFERRED, GetNotifyFlags, GetNotifyFlags method [BITS], GetNotifyFlags method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetNotifyFlags method, IBackgroundCopyJob.GetNotifyFlags, IBackgroundCopyJob::GetNotifyFlags, _drz_ibackgroundcopyjob_getnotifyflags, bits.ibackgroundcopyjob_getnotifyflags, bits/IBackgroundCopyJob::GetNotifyFlags
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
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob::GetNotifyFlags
 - bits/IBackgroundCopyJob::GetNotifyFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetNotifyFlags
---

# IBackgroundCopyJob::GetNotifyFlags


## -description

Retrieves the event notification flags for the job.

## -parameters

### -param pVal [out]

Identifies the events that your application receives. The following table lists the event notification flag values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_JOB_TRANSFERRED"></a><a id="bg_notify_job_transferred"></a><dl>
<dt><b>BG_NOTIFY_JOB_TRANSFERRED</b></dt>
</dl>
</td>
<td width="60%">
All of the files in the job have been transferred.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_JOB_ERROR"></a><a id="bg_notify_job_error"></a><dl>
<dt><b>BG_NOTIFY_JOB_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error has occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_DISABLE"></a><a id="bg_notify_disable"></a><dl>
<dt><b>BG_NOTIFY_DISABLE</b></dt>
</dl>
</td>
<td width="60%">
Event notification is disabled. If set, BITS ignores the other flags.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_JOB_MODIFICATION"></a><a id="bg_notify_job_modification"></a><dl>
<dt><b>BG_NOTIFY_JOB_MODIFICATION</b></dt>
</dl>
</td>
<td width="60%">
The job has been modified.

</td>
</tr>
</table>

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

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
Event notify flags were successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Must pass the address of <i>pNotifyFlags</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnotifyinterface">IBackgroundCopyJob::GetNotifyInterface</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a>