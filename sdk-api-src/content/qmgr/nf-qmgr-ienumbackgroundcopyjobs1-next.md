---
UID: NF:qmgr.IEnumBackgroundCopyJobs1.Next
title: IEnumBackgroundCopyJobs1::Next
author: windows-sdk-content
description: Use the Next method to retrieve the specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.
old-location: bits\ienumbackgroundcopyjobs1_next.htm
old-project: Bits
ms.assetid: 15dcc2e1-7fdf-4c4a-a24b-2cad49bda7fc
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IEnumBackgroundCopyJobs1 interface [BITS],Next method, IEnumBackgroundCopyJobs1.Next, IEnumBackgroundCopyJobs1::Next, Next, Next method [BITS], Next method [BITS],IEnumBackgroundCopyJobs1 interface, bits.ienumbackgroundcopyjobs1_next, qmgr/IEnumBackgroundCopyJobs1::Next
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
 - IEnumBackgroundCopyJobs1.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumBackgroundCopyJobs1::Next


## -description


<p class="CCE_Message">[<b>IEnumBackgroundCopyJobs1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>Next</b> method to retrieve the specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.


## -parameters




### -param celt [in]

Number of elements requested.


### -param rgelt [out]

Array of GUIDs that identify the jobs. To retrieve a job, call the <a href="https://msdn.microsoft.com/c392e9e2-0489-457b-b21a-dfff9e2c0f39">IBackgroundCopyGroup::GetJob</a> method with the GUID.


### -param pceltFetched [out]

Number of elements in <i>rgelt</i>. You can set <i>pceltFetched</i> to <b>NULL</b> if <i>celt</i> is one.


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
Successfully returned the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returned less than the number of requested elements.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/93feac90-8eb8-49d8-9841-d78a2645fbcb">IEnumBackgroundCopyJobs1</a>
 

 

