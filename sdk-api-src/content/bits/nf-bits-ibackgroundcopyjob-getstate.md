---
UID: NF:bits.IBackgroundCopyJob.GetState
title: IBackgroundCopyJob::GetState
author: windows-sdk-content
description: Retrieves the state of the job.
old-location: bits\ibackgroundcopyjob_getstate.htm
tech.root: bits
ms.assetid: 32789bd2-2368-473b-accf-ac6e317d0172
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetState, GetState method [BITS], GetState method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetState method, IBackgroundCopyJob.GetState, IBackgroundCopyJob::GetState, _drz_ibackgroundcopyjob_getstate, bits.ibackgroundcopyjob_getstate, bits/IBackgroundCopyJob::GetState
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
 - IBackgroundCopyJob.GetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::GetState


## -description


Retrieves the state of the job.


## -parameters




### -param pVal [out]

The state of the job. For example, the state reflects whether the job is in error, transferring data, or suspended. For a list of job states, see the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362809(v=VS.85).aspx">BG_JOB_STATE</a> enumeration.


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
<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a> interface.


#### Examples

See the example code for the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363060(v=VS.85).aspx">IBackgroundCopyManager::GetJob</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362809(v=VS.85).aspx">BG_JOB_STATE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362836(v=VS.85).aspx">Determining the Status of a Job</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a>
 

 

