---
UID: NF:bits.IBackgroundCopyJob.SetNotifyInterface
title: IBackgroundCopyJob::SetNotifyInterface (bits.h)
description: Identifies your implementation of the IBackgroundCopyCallback interface to BITS. Use the IBackgroundCopyCallback interface to receive notification of job-related events.
helpviewer_keywords: ["IBackgroundCopyJob interface [BITS]","SetNotifyInterface method","IBackgroundCopyJob.SetNotifyInterface","IBackgroundCopyJob::SetNotifyInterface","SetNotifyInterface","SetNotifyInterface method [BITS]","SetNotifyInterface method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_setnotifyinterface","bits.ibackgroundcopyjob_setnotifyinterface","bits/IBackgroundCopyJob::SetNotifyInterface"]
old-location: bits\ibackgroundcopyjob_setnotifyinterface.htm
tech.root: Bits
ms.assetid: 34d51546-ec27-471f-9da5-3bec7ed4e1ea
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetNotifyInterface method, IBackgroundCopyJob.SetNotifyInterface, IBackgroundCopyJob::SetNotifyInterface, SetNotifyInterface, SetNotifyInterface method [BITS], SetNotifyInterface method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setnotifyinterface, bits.ibackgroundcopyjob_setnotifyinterface, bits/IBackgroundCopyJob::SetNotifyInterface
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
 - IBackgroundCopyJob::SetNotifyInterface
 - bits/IBackgroundCopyJob::SetNotifyInterface
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
 - IBackgroundCopyJob.SetNotifyInterface
---

# IBackgroundCopyJob::SetNotifyInterface


## -description

Identifies your implementation of the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface to BITS. Use the 
<b>IBackgroundCopyCallback</b> interface to receive notification of job-related events.

## -parameters

### -param Val

An 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface pointer. To remove the current callback interface pointer, set this parameter to <b>NULL</b>.

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
Notification interface pointer was successfully set.

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

Call this method only if you implement the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface. Use the 
<b>SetNotifyInterface</b> method in conjunction with the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">SetNotifyFlags</a> method to specify the type of notification that you want to receive. 

The notification interface becomes invalid when your application terminates; BITS does not persist the notify interface. As a result, your application's initialization process should call the 
<b>SetNotifyInterface</b> method on those existing jobs for which you want to receive notification. If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.

Note that BITS will call your callback even if the event for which you registered already occurred.

As an alternative to receiving callback notification, you can register to have BITS execute a command line for error and transferred events. For more details, see the 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">IBackgroundCopyJob2::SetNotifyCmdLine</a> method.

Note that if more than one application calls the  <b>SetNotifyInterface</b> method to set the notification interface for the job, the last application to call the <b>SetNotifyInterface</b> method is the one that will receive notifications—the other applications will not receive notifications.


#### Examples

The following example shows how to call the 
<b>SetNotifyInterface</b> method. For details on the CNotifyInterface example class used in the following example, see the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface. The example assumes the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> interface pointer is valid.


```cpp
IBackgroundCopyJob* pJob;
CNotifyInterface* pNotify = new CNotifyInterface();

hr = pJob->SetNotifyInterface(pNotify);
if (SUCCEEDED(hr))
{
  hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                            BG_NOTIFY_JOB_ERROR);
}
pNotify->Release();
pNofity = NULL;

if (FAILED(hr))
{
  //Handle error - unable to register for event notification.
}
```

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">IBackgroundCopyJob2::SetNotifyCmdLine</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnotifyinterface">IBackgroundCopyJob::GetNotifyInterface</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a>