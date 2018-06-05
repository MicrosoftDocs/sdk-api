---
UID: NF:winsync.IEnumFeedClockVector.Skip
title: IEnumFeedClockVector::Skip
author: windows-sdk-content
description: Skips the specified number of clock vector elements.
old-location: winsync\ienumfeedclockvector_skip.htm
old-project: winsync
ms.assetid: eabe3389-2c1f-4b0e-a062-24bbe3fa87f9
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IEnumFeedClockVector interface [Windows Sync],Skip method, IEnumFeedClockVector.Skip, IEnumFeedClockVector::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumFeedClockVector interface, winsync.ienumfeedclockvector_skip, winsync/IEnumFeedClockVector::Skip
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IEnumFeedClockVector.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumFeedClockVector::Skip


## -description


Skips the specified number of clock vector elements.


## -parameters




### -param cSyncVersions [in]

The number of elements to skip.


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
The enumerator reaches the end of its list before it can skip <i>cSyncVersions</i> elements. In this case, the enumerator skips as many elements as possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/87679327-3a09-4416-b802-91171feb160a">IEnumFeedClockVector Interface</a>
 

 

