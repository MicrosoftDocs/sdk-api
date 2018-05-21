---
UID: NF:qmgr.IEnumBackgroundCopyJobs1.Skip
title: IEnumBackgroundCopyJobs1::Skip
author: windows-driver-content
description: Use the Skip method to skip the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.
old-location: bits\ienumbackgroundcopyjobs1_skip.htm
old-project: Bits
ms.assetid: b388530c-688a-46a9-ae23-370f902b870e
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IEnumBackgroundCopyJobs1 interface [BITS],Skip method, IEnumBackgroundCopyJobs1.Skip, IEnumBackgroundCopyJobs1::Skip, Skip, Skip method [BITS], Skip method [BITS],IEnumBackgroundCopyJobs1 interface, bits.ienumbackgroundcopyjobs1_skip, qmgr/IEnumBackgroundCopyJobs1::Skip
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
-	IEnumBackgroundCopyJobs1.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumBackgroundCopyJobs1::Skip


## -description


<p class="CCE_Message">[<b>IEnumBackgroundCopyJobs1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>Skip</b> method to skip the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


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
Successfully skipped the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped less than the number of requested elements.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/93feac90-8eb8-49d8-9841-d78a2645fbcb">IEnumBackgroundCopyJobs1</a>
 

 

