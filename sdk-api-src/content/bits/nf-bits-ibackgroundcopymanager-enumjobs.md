---
UID: NF:bits.IBackgroundCopyManager.EnumJobs
title: IBackgroundCopyManager::EnumJobs
author: windows-sdk-content
description: Retrieves an interface pointer to an enumerator object that you use to enumerate the jobs in the transfer queue. The order of the jobs in the enumerator is arbitrary.
old-location: bits\ibackgroundcopymanager_enumjobs.htm
old-project: bits
ms.assetid: e8b73060-dff9-4ab3-8009-d2b41502fc1a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BG_JOB_ENUM_ALL_USERS, EnumJobs, EnumJobs method [BITS], EnumJobs method [BITS],IBackgroundCopyManager interface, IBackgroundCopyManager interface [BITS],EnumJobs method, IBackgroundCopyManager.EnumJobs, IBackgroundCopyManager::EnumJobs, _drz_ibackgroundcopymanager_enumjobs, bits.ibackgroundcopymanager_enumjobs, bits/IBackgroundCopyManager::EnumJobs
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
 - IBackgroundCopyManager.EnumJobs
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyManager::EnumJobs


## -description


Retrieves an interface pointer to an enumerator object that you use to 
<a href="https://msdn.microsoft.com/ebeb1670-dedd-4791-914e-d035d3c22c5a">enumerate the jobs</a> in the transfer queue. The order of the jobs in the enumerator is arbitrary.


## -parameters




### -param dwFlags [in]

Specifies whose jobs to include in the enumeration. If <i>dwFlags</i> is set to 0, the user receives all jobs that they own in the transfer queue. The following table lists the enumeration options. 



<table>
<tr>
<th>Option</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_JOB_ENUM_ALL_USERS"></a><a id="bg_job_enum_all_users"></a><dl>
<dt><b>BG_JOB_ENUM_ALL_USERS</b></dt>
</dl>
</td>
<td width="60%">
Includes all jobs in the transfer queue—those owned by the user and those owned by others. The user must be an administrator to use this flag.

</td>
</tr>
</table>
 


### -param ppEnum






#### - ppEnumJobs [out]

An 
<a href="https://msdn.microsoft.com/21ff88da-9fae-478f-bcba-488ed7a89608">IEnumBackgroundCopyJobs</a> interface pointer that you use to enumerate the jobs in the transfer queue. The contents of the enumerator depend on the value of <i>dwFlags</i>. Release <i>ppEnumJobs</i> when done.


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
Successfully generated enumerator object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The user must be an administrator or belong to an administrator group to enumerate jobs owned by another user.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c6b8ef69-9c67-447f-9f90-b6905a5a5a19">IBackgroundCopyJob::EnumFiles</a>



<a href="https://msdn.microsoft.com/dbb7cae6-7e9c-4ac5-8f02-372acaa4fb4d">IBackgroundCopyManager::GetJob</a>



<a href="https://msdn.microsoft.com/21ff88da-9fae-478f-bcba-488ed7a89608">IEnumBackgroundCopyJobs</a>
 

 

