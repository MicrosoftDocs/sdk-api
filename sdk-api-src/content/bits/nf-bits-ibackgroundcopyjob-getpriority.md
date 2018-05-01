---
UID: NF:bits.IBackgroundCopyJob.GetPriority
title: IBackgroundCopyJob::GetPriority method
author: windows-driver-content
description: Retrieves the priority level for the job. The priority level determines when the job is processed relative to other jobs in the transfer queue.
old-location: bits\ibackgroundcopyjob_getpriority.htm
old-project: Bits
ms.assetid: 8602ed59-a372-4cb3-bbda-cf1c7afc3669
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: GetPriority method [BITS], GetPriority method [BITS], IBackgroundCopyJob interface, GetPriority,IBackgroundCopyJob.GetPriority, IBackgroundCopyJob, IBackgroundCopyJob interface [BITS], GetPriority method, IBackgroundCopyJob::GetPriority, _drz_ibackgroundcopyjob_getpriority, bits.ibackgroundcopyjob_getpriority, bits/IBackgroundCopyJob::GetPriority
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
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyJob.GetPriority
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::GetPriority method


## -description


Retrieves the priority level for the job. The priority level determines when the job is processed relative to other jobs in the transfer queue.


## -parameters




### -param pVal






#### - pPriority [out]

Priority of the job relative to other jobs in the transfer queue.


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
Priority level was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPriority</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e">BG_JOB_PRIORITY</a>



<a href="https://msdn.microsoft.com/8b59128d-7e63-45dc-af0f-54ea844dac98">IBackgroundCopyJob::SetPriority</a>
 

 

