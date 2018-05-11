---
UID: NF:winsync.IEnumFeedClockVector.Next
title: IEnumFeedClockVector::Next
author: windows-driver-content
description: Returns the next elements in the clock vector, if available.
old-location: winsync\ienumfeedclockvector_next.htm
old-project: winsync
ms.assetid: 2303fac8-21ae-44df-8e47-9fe0fa88d90b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IEnumFeedClockVector interface [Windows Sync],Next method, IEnumFeedClockVector.Next, IEnumFeedClockVector::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumFeedClockVector interface, winsync.ienumfeedclockvector_next, winsync/IEnumFeedClockVector::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IEnumFeedClockVector.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumFeedClockVector::Next


## -description


Returns the next elements in the clock vector, if available.


## -parameters




### -param cClockVectorElements [in]

The number of clock vector elements to retrieve.


### -param ppiClockVectorElements [out]

Returns the next <i>pcFetched</i> clock vector elements.


### -param pcFetched [in, out]

Returns the number of clock vector elements that were retrieved. This value can be <b>NULL</b> if <i>cClockVectorElements</i> is 1; otherwise, it cannot be <b>NULL</b>.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
If there are no more elements to retrieve.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/87679327-3a09-4416-b802-91171feb160a">IEnumFeedClockVector Interface</a>
 

 

