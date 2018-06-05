---
UID: NF:bits.IBackgroundCopyJob.SetPriority
title: IBackgroundCopyJob::SetPriority
author: windows-sdk-content
description: Specifies the priority level of your job. The priority level determines when your job is processed relative to other jobs in the transfer queue.
old-location: bits\ibackgroundcopyjob_setpriority.htm
old-project: Bits
ms.assetid: 8b59128d-7e63-45dc-af0f-54ea844dac98
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetPriority method, IBackgroundCopyJob.SetPriority, IBackgroundCopyJob::SetPriority, SetPriority, SetPriority method [BITS], SetPriority method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setpriority, bits.ibackgroundcopyjob_setpriority, bits/IBackgroundCopyJob::SetPriority
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyJob.SetPriority
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::SetPriority


## -description


Specifies the priority level of your job. The priority level determines when your job is processed relative to other jobs in the transfer queue.


## -parameters




### -param Val






#### - Priority [in]

Specifies the priority level of your job relative to other jobs in the transfer queue. The default is BG_JOB_PRIORITY_NORMAL. For a list of priority levels, see the 
<a href="https://msdn.microsoft.com/bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e">BG_JOB_PRIORITY</a> enumeration.


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
Job priority was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>Priority</i> is not defined in the 
<a href="https://msdn.microsoft.com/bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e">BG_JOB_PRIORITY</a> enumeration.

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




<a href="https://msdn.microsoft.com/bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e">BG_JOB_PRIORITY</a>



<a href="https://msdn.microsoft.com/8602ed59-a372-4cb3-bbda-cf1c7afc3669">IBackgroundCopyJob::GetPriority</a>
 

 

