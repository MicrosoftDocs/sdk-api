---
UID: NF:qmgr.IBackgroundCopyGroup.CreateJob
title: IBackgroundCopyGroup::CreateJob
author: windows-sdk-content
description: Use the CreateJob method to add a new job to the group. A group can contain only one job.
old-location: bits\ibackgroundcopygroup_createjob.htm
old-project: Bits
ms.assetid: 2453996e-f994-43b9-901b-680a55095268
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CreateJob, CreateJob method [BITS], CreateJob method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],CreateJob method, IBackgroundCopyGroup.CreateJob, IBackgroundCopyGroup::CreateJob, bits.ibackgroundcopygroup_createjob, qmgr/IBackgroundCopyGroup::CreateJob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GROUPPROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup.CreateJob
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: ADAM
---

# IBackgroundCopyGroup::CreateJob


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>CreateJob</b> method to add a new job to the group. A group can contain only one job.


## -parameters




### -param guidJobID




### -param ppJob [out]

Pointer to an <a href="https://msdn.microsoft.com/ccf1b355-c1af-4b5e-b613-181c426ed777">IBackgroundCopyJob1</a> interface pointer. Use the interface to add files and check the state of the job.


#### - guidJobId [in]

Uniquely identifies the job in the group and queue.


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
The job was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QM_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The job is already running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Only one job allowed per group.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

