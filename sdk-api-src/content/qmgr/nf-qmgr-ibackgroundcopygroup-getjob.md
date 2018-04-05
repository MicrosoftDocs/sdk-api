---
UID: NF:qmgr.IBackgroundCopyGroup.GetJob
title: IBackgroundCopyGroup::GetJob method
author: windows-driver-content
description: Use the GetJob method to retrieve a job from the group.
old-location: bits\ibackgroundcopygroup_getjob.htm
old-project: Bits
ms.assetid: c392e9e2-0489-457b-b21a-dfff9e2c0f39
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetJob method [BITS], GetJob method [BITS], IBackgroundCopyGroup interface, GetJob,IBackgroundCopyGroup.GetJob, IBackgroundCopyGroup, IBackgroundCopyGroup interface [BITS], GetJob method, IBackgroundCopyGroup::GetJob, bits.ibackgroundcopygroup_getjob, qmgr/IBackgroundCopyGroup::GetJob
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: GROUPPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyGroup.GetJob
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IBackgroundCopyGroup::GetJob method


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>GetJob</b> method to retrieve a job from the group.


## -parameters




### -param jobID




### -param ppJob [out]

Pointer to an <a href="https://msdn.microsoft.com/ccf1b355-c1af-4b5e-b613-181c426ed777">IBackgroundCopyJob1</a> interface pointer. Use the interface to add files and retrieve the state of the job.


#### - guidJobId [in]

Identifies the job to retrieve.


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
Successfully retrieved the job from the group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QM_E_ITEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find the job in the group.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

