---
UID: NF:bits.IBackgroundCopyJob.SetNotifyFlags
title: IBackgroundCopyJob::SetNotifyFlags (bits.h)
description: Specifies the type of event notification you want to receive, such as job transferred events.
helpviewer_keywords: ["BG_NOTIFY_DISABLE","BG_NOTIFY_FILE_RANGES_TRANSFERRED","BG_NOTIFY_FILE_TRANSFERRED","BG_NOTIFY_JOB_ERROR","BG_NOTIFY_JOB_MODIFICATION","BG_NOTIFY_JOB_TRANSFERRED","IBackgroundCopyJob interface [BITS]","SetNotifyFlags method","IBackgroundCopyJob.SetNotifyFlags","IBackgroundCopyJob::SetNotifyFlags","SetNotifyFlags","SetNotifyFlags method [BITS]","SetNotifyFlags method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_setnotifyflags","bits.ibackgroundcopyjob_setnotifyflags","bits/IBackgroundCopyJob::SetNotifyFlags"]
old-location: bits\ibackgroundcopyjob_setnotifyflags.htm
tech.root: Bits
ms.assetid: 24aa6445-d7bd-4825-9121-402e63ae6f69
ms.date: 12/05/2018
ms.keywords: BG_NOTIFY_DISABLE, BG_NOTIFY_FILE_RANGES_TRANSFERRED, BG_NOTIFY_FILE_TRANSFERRED, BG_NOTIFY_JOB_ERROR, BG_NOTIFY_JOB_MODIFICATION, BG_NOTIFY_JOB_TRANSFERRED, IBackgroundCopyJob interface [BITS],SetNotifyFlags method, IBackgroundCopyJob.SetNotifyFlags, IBackgroundCopyJob::SetNotifyFlags, SetNotifyFlags, SetNotifyFlags method [BITS], SetNotifyFlags method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setnotifyflags, bits.ibackgroundcopyjob_setnotifyflags, bits/IBackgroundCopyJob::SetNotifyFlags
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
 - IBackgroundCopyJob::SetNotifyFlags
 - bits/IBackgroundCopyJob::SetNotifyFlags
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
 - IBackgroundCopyJob.SetNotifyFlags
---

# IBackgroundCopyJob::SetNotifyFlags


## -description

Specifies the type of event notification you want to receive, such as job transferred events.

## -parameters

### -param Val [in]

Set one or more of the following flags to identify the events that you want to receive.  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_JOB_TRANSFERRED"></a><a id="bg_notify_job_transferred"></a><dl>
<dt><b>BG_NOTIFY_JOB_TRANSFERRED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
All of the files in the job have been transferred.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_JOB_ERROR"></a><a id="bg_notify_job_error"></a><dl>
<dt><b>BG_NOTIFY_JOB_ERROR</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
An error has occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_DISABLE"></a><a id="bg_notify_disable"></a><dl>
<dt><b>BG_NOTIFY_DISABLE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Event notification is disabled. BITS ignores the other flags.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_JOB_MODIFICATION"></a><a id="bg_notify_job_modification"></a><dl>
<dt><b>BG_NOTIFY_JOB_MODIFICATION</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The job has been modified. For example, a property value changed, the state of the job changed, or progress is made transferring the files. This flag is ignored in command-line callbacks if 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">command line notification</a> is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_FILE_TRANSFERRED"></a><a id="bg_notify_file_transferred"></a><dl>
<dt><b>BG_NOTIFY_FILE_TRANSFERRED</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
A file in the job has been transferred.  This flag is ignored in command-line callbacks if 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">command line notification</a> is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></a><a id="bg_notify_file_ranges_transferred"></a><dl>
<dt><b>BG_NOTIFY_FILE_RANGES_TRANSFERRED</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
A range of bytes in the file has been transferred.    This flag is ignored in command-line callbacks if 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">command line notification</a> is specified. The flag can be specified for any job, but you will only get notifications for jobs that meet the requirements for a <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> job.

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
Type of event notification was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The <i>NotifyFlags</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
</table>

## -remarks

Use the 
<b>SetNotifyFlags</b> method in conjunction with the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a> and 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">IBackgroundCopyJob2::SetNotifyCmdLine</a> methods to receive event notification.


#### Examples

See the example code for the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a> method.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopycallback2">IBackgroundCopyCallback2</a>



<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">IBackgroundCopyJob2::SetNotifyCmdLine</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnotifyflags">IBackgroundCopyJob::GetNotifyFlags</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a>