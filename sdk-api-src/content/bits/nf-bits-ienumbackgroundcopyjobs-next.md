---
UID: NF:bits.IEnumBackgroundCopyJobs.Next
title: IEnumBackgroundCopyJobs::Next
author: windows-sdk-content
description: Retrieves a specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.
old-location: bits\ienumbackgroundcopyjobs_next.htm
old-project: Bits
ms.assetid: a248e14a-ab17-4e8e-9e27-2ba31a4a999d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IEnumBackgroundCopyJobs interface [BITS],Next method, IEnumBackgroundCopyJobs.Next, IEnumBackgroundCopyJobs::Next, Next, Next method [BITS], Next method [BITS],IEnumBackgroundCopyJobs interface, _drz_ienumbackgroundcopyjobs_next, bits.ienumbackgroundcopyjobs_next, bits/IEnumBackgroundCopyJobs::Next
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IEnumBackgroundCopyJobs.Next
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IEnumBackgroundCopyJobs::Next


## -description


Retrieves a specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.


## -parameters




### -param celt [in]

Number of elements requested.


### -param rgelt [out]

Array of 
<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> objects. You must release each object in <i>rgelt</i> when done.


### -param pceltFetched [out]

Number of elements returned in <i>rgelt</i>. You can set <i>pceltFetched</i> to <b>NULL</b> if <i>celt</i> is one. Otherwise, initialize the value of <i>pceltFetched</i> to 0 before calling this method.


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




<a href="https://msdn.microsoft.com/21ff88da-9fae-478f-bcba-488ed7a89608">IEnumBackgroundCopyJobs</a>
 

 

