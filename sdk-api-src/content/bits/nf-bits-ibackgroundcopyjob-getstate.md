---
UID: NF:bits.IBackgroundCopyJob.GetState
title: IBackgroundCopyJob::GetState
author: windows-sdk-content
description: Retrieves the state of the job.
old-location: bits\ibackgroundcopyjob_getstate.htm
old-project: Bits
ms.assetid: 32789bd2-2368-473b-accf-ac6e317d0172
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetState, GetState method [BITS], GetState method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetState method, IBackgroundCopyJob.GetState, IBackgroundCopyJob::GetState, _drz_ibackgroundcopyjob_getstate, bits.ibackgroundcopyjob_getstate, bits/IBackgroundCopyJob::GetState
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetState
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::GetState


## -description


Retrieves the state of the job.


## -parameters




### -param pVal






#### - pJobState [out]

The state of the job. For example, the state reflects whether the job is in error, transferring data, or suspended. For a list of job states, see the 
<a href="https://msdn.microsoft.com/a7857cf1-05b7-42df-b79e-50a2f6a406dc">BG_JOB_STATE</a> enumeration.


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
The state of the job was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter, <i>pJobState</i>, cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when  events occur. For details on registering to receive event notification, see the 
<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a> interface.


#### Examples

See the example code for the 
<a href="https://msdn.microsoft.com/dbb7cae6-7e9c-4ac5-8f02-372acaa4fb4d">IBackgroundCopyManager::GetJob</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a7857cf1-05b7-42df-b79e-50a2f6a406dc">BG_JOB_STATE</a>



<a href="https://msdn.microsoft.com/7c6cdf86-196d-41b3-ae45-9728b8092c30">Determining the Status of a Job</a>



<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a>
 

 

