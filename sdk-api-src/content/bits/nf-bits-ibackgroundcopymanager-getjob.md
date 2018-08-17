---
UID: NF:bits.IBackgroundCopyManager.GetJob
title: IBackgroundCopyManager::GetJob
author: windows-sdk-content
description: Retrieves a specified job from the transfer queue. Typically, your application persists the job identifier, so you can later retrieve the job from the queue.
old-location: bits\ibackgroundcopymanager_getjob.htm
old-project: bits
ms.assetid: dbb7cae6-7e9c-4ac5-8f02-372acaa4fb4d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetJob, GetJob method [BITS], GetJob method [BITS],IBackgroundCopyManager interface, IBackgroundCopyManager interface [BITS],GetJob method, IBackgroundCopyManager.GetJob, IBackgroundCopyManager::GetJob, _drz_ibackgroundcopymanager_getjob, bits.ibackgroundcopymanager_getjob, bits/IBackgroundCopyManager::GetJob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
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
 - IBackgroundCopyManager.GetJob
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyManager::GetJob


## -description


Retrieves a specified job from the transfer queue. Typically, your application persists the job identifier, so you can later retrieve the job from the queue.


## -parameters




### -param jobID




### -param ppJob [out]

An 
<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a> interface pointer to the job specified by <i>JobID</i>. When done, release <i>ppJob</i>.


#### - JobID [in]

Identifies the job to retrieve from the transfer queue. The 
<a href="https://msdn.microsoft.com/en-us/library/Aa363051(v=VS.85).aspx">CreateJob</a> method returns the job identifier.


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
Job was successfully retrieved from the transfer queue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The job was not found in the queue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
User does not have permission to retrieve the job.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363027(v=VS.85).aspx">IBackgroundCopyJob::GetId</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363051(v=VS.85).aspx">IBackgroundCopyManager::CreateJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363052(v=VS.85).aspx">IBackgroundCopyManager::EnumJobs</a>
 

 

