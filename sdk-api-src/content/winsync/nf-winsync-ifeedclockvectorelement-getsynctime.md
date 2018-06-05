---
UID: NF:winsync.IFeedClockVectorElement.GetSyncTime
title: IFeedClockVectorElement::GetSyncTime
author: windows-sdk-content
description: Gets a SYNC_TIME value that corresponds to the when value for the item.
old-location: winsync\ifeedclockvectorelement_getsynctime.htm
old-project: winsync
ms.assetid: f39b3bdf-a37e-4673-a620-5b14109718cb
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSyncTime, GetSyncTime method [Windows Sync], GetSyncTime method [Windows Sync],IFeedClockVectorElement interface, IFeedClockVectorElement interface [Windows Sync],GetSyncTime method, IFeedClockVectorElement.GetSyncTime, IFeedClockVectorElement::GetSyncTime, winsync.ifeedclockvectorelement_getsynctime, winsync/IFeedClockVectorElement::GetSyncTime
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
-	IFeedClockVectorElement.GetSyncTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IFeedClockVectorElement::GetSyncTime


## -description


Gets a <a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME</a> value that corresponds to the <b>when</b> value for the item.


## -parameters




### -param pSyncTime [out]

Returns a <a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME</a> value that corresponds to the <b>when</b> value for the item.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME</a> structure is a packed date-and-time value that can store years between 1601 and 67136 and times that are accurate to the millisecond.




## -see-also




<a href="https://msdn.microsoft.com/7ffc228f-c4f2-4451-9b23-ec78bf6c8318">IFeedClockVectorElement Interface</a>



<a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME Structure</a>
 

 

