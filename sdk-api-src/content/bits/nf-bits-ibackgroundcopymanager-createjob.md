---
UID: NF:bits.IBackgroundCopyManager.CreateJob
title: IBackgroundCopyManager::CreateJob
author: windows-sdk-content
description: Creates a job.
old-location: bits\ibackgroundcopymanager_createjob.htm
old-project: bits
ms.assetid: 6d23e3c0-673b-4f37-b6a0-e364b2d73886
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateJob, CreateJob method [BITS], CreateJob method [BITS],IBackgroundCopyManager interface, IBackgroundCopyManager interface [BITS],CreateJob method, IBackgroundCopyManager.CreateJob, IBackgroundCopyManager::CreateJob, _drz_ibackgroundcopymanager_createjob, bits.ibackgroundcopymanager_createjob, bits/IBackgroundCopyManager::CreateJob
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
 - IBackgroundCopyManager.CreateJob
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyManager::CreateJob


## -description


 
Creates a job.


## -parameters




### -param DisplayName




### -param Type [in]

Type of transfer job, such as BG_JOB_TYPE_DOWNLOAD. For a list of transfer types, see the 
<a href="https://msdn.microsoft.com/b341a63f-3a1d-4518-8f05-17d28af603b4">BG_JOB_TYPE</a> enumeration.


### -param pJobId




### -param ppJob [out]

An 
<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> interface pointer that you use to modify the job's properties and specify the files to be transferred. To activate the job in the queue, call the 
<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> method. Release <i>ppJob</i> when done.


#### - pDisplayName [in]

Null-terminated string that contains a display name for the job. Typically, the display name is used to identify the job in a user interface. Note that more than one job may have the same display name. Must not be <b>NULL</b>. The name is limited to 256 characters, not including the null terminator.


#### - pJobID [out]

Uniquely identifies your job in the queue. Use this identifier when you call the 
<a href="https://msdn.microsoft.com/dbb7cae6-7e9c-4ac5-8f02-372acaa4fb4d">IBackgroundCopyManager::GetJob</a> method to get a job from the queue.


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
Successfully generated the new job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The display name is too long.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_TOO_MANY_JOBS_PER_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The MaxJobsPerMachine Group Policy setting determines how many jobs can be created on the computer. Adding this job exceeds the MaxJobsPerMachine limit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_TOO_MANY_JOBS_PER_USER</b></dt>
</dl>
</td>
<td width="60%">
The MaxJobsPerUser Group Policy setting determines how many jobs a user can create. Adding this job exceeds the MaxJobsPerUser limit.

</td>
</tr>
</table>
 




## -remarks



Only the user who creates the job or a user with administrator privileges can <a href="https://msdn.microsoft.com/fb6e7219-b6ca-4f72-b7a3-60d65e8f3892">add files to the job</a> and <a href="https://msdn.microsoft.com/5d0ab96b-b818-4b41-8317-cf50ad17c12d">change the job's properties</a>.

By default, BITS supports a maximum of 300 jobs at one time. A single user can create a maximum of 60 jobs at one time. The user limit does not apply to administrators or service accounts. To change these defaults, set the <b>MaxJobsPerMachine</b> and <b>MaxJobsPerUser</b> group policies, respectively.

<b>Prior to Windows Vista:  </b>There is no limit on the number of jobs that BITS supports or that a user can create.

For scalability concerns, see <a href="https://msdn.microsoft.com/f4a09a80-2a85-4b59-b0fd-c23c128973f7">Best Practices When Using BITS</a>.


#### Examples

For an example that creates a new job, see 
<a href="https://msdn.microsoft.com/a7d9feef-4beb-4ae5-9453-9157ee3ec0e8">Creating a Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a7d9feef-4beb-4ae5-9453-9157ee3ec0e8">Creating a Job</a>



<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a>
 

 

