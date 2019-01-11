---
UID: NF:bits.IBackgroundCopyJob.Suspend
title: IBackgroundCopyJob::Suspend
author: windows-sdk-content
description: Suspends a job. New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.
old-location: bits\ibackgroundcopyjob_suspend.htm
tech.root: Bits
ms.assetid: 88429730-b8e5-4969-934c-f0945fdd46a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyJob interface [BITS],Suspend method, IBackgroundCopyJob.Suspend, IBackgroundCopyJob::Suspend, Suspend, Suspend method [BITS], Suspend method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_suspend, bits.ibackgroundcopyjob_suspend, bits/IBackgroundCopyJob::Suspend
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
 - IBackgroundCopyJob.Suspend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::Suspend


## -description


Suspends a job. New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.


## -parameters






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
Successfully suspended the job.

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
 




## -see-also




<a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a>



<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a>
 

 

