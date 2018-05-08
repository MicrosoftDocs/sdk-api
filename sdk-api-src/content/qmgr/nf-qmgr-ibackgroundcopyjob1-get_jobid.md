---
UID: NF:qmgr.IBackgroundCopyJob1.get_JobID
title: IBackgroundCopyJob1::get_JobID
author: windows-driver-content
description: Use the get_JobID method to retrieve the job's identifier.
old-location: bits\ibackgroundcopyjob1_get_jobid.htm
old-project: Bits
ms.assetid: 4f639576-33fd-413c-a163-764c0aa2ce81
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: IBackgroundCopyJob1 interface [BITS],get_JobID method, IBackgroundCopyJob1.get_JobID, IBackgroundCopyJob1::get_JobID, bits.ibackgroundcopyjob1_get_jobid, get_JobID, get_JobID method [BITS], get_JobID method [BITS],IBackgroundCopyJob1 interface, qmgr/IBackgroundCopyJob1::get_JobID
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
-	IBackgroundCopyJob1.get_JobID
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IBackgroundCopyJob1::get_JobID


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/ccf1b355-c1af-4b5e-b613-181c426ed777">IBackgroundCopyJob1</a> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>get_JobID</b> method to retrieve the job's identifier.


## -parameters




### -param pguidJobID






#### - pguidJobId [out]

GUID that uniquely identifies the job.


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
Successfully retrieved the GUID that identifies the job.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ccf1b355-c1af-4b5e-b613-181c426ed777">IBackgroundCopyJob1</a>
 

 

