---
UID: NF:bits.IBackgroundCopyJob.SetNoProgressTimeout
title: IBackgroundCopyJob::SetNoProgressTimeout
author: windows-sdk-content
description: Sets the length of time that BITS tries to transfer the file after a transient error condition occurs. If there is progress, the timer is reset.
old-location: bits\ibackgroundcopyjob_setnoprogresstimeout.htm
tech.root: Bits
ms.assetid: 3fcf46ed-197f-46ad-ac62-2c4a2e8b27ef
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetNoProgressTimeout method, IBackgroundCopyJob.SetNoProgressTimeout, IBackgroundCopyJob::SetNoProgressTimeout, SetNoProgressTimeout, SetNoProgressTimeout method [BITS], SetNoProgressTimeout method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setnoprogresstimeout, bits.ibackgroundcopyjob_setnoprogresstimeout, bits/IBackgroundCopyJob::SetNoProgressTimeout
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.SetNoProgressTimeout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bits.h
: 
- IBackgroundCopyJob.SetNoProgressTimeout
: 
---

# IBackgroundCopyJob::SetNoProgressTimeout


## -description


Sets the length of time that BITS tries to transfer the file after a transient error condition occurs. If there is progress, the timer is reset.


## -parameters




### -param Seconds

TBD




#### - RetryPeriod [in]

Length of time, in seconds, that BITS tries to transfer the file after the first transient error occurs. The default retry period is 1,209,600 seconds (14 days). Set the retry period to 0 to prevent retries and to force the job into the BG_JOB_STATE_ERROR state for all errors. If the retry period value exceeds the <a href="https://msdn.microsoft.com/32c7e2b1-bac2-4708-a30c-f6b2a816c1a4">JobInactivityTimeout</a> Group Policy value (90-day default), BITS cancels the job after the policy value is exceeded.  


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Retry period successfully set.

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



If BITS does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR. If you request error notification, BITS then calls your 
<a href="https://msdn.microsoft.com/3e206195-1a8c-435e-9b8f-6517b8e3c4ca">JobError</a> callback.

<b>Note</b>  Changing the system clock does not affect the retry period. For example, if the retry period expires in 14 days, moving the system clock forward 14 or more days does not mean the retry period expires early—the retry period will still expire in 14 days. To reflect the system clock change in BITS, you must restart the computer or the BITS service.




## -see-also




<a href="https://msdn.microsoft.com/4881e5f7-a835-40d5-a056-d6b23e3cd84c">IBackgroundCopyJob::GetNoProgressTimeout</a>



<a href="https://msdn.microsoft.com/52d2b7a1-6f68-424e-9c0b-a9f8df4a5ad6">IBackgroundCopyJob::SetMinimumRetryDelay</a>
 

 

