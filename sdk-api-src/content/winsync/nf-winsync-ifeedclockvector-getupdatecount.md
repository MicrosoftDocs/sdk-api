---
UID: NF:winsync.IFeedClockVector.GetUpdateCount
title: IFeedClockVector::GetUpdateCount
author: windows-sdk-content
description: Gets the number of updates that have been made to the FeedSync item.
old-location: winsync\ifeedclockvector_getupdatecount.htm
tech.root: winsync
ms.assetid: a8cf6b0f-2049-4047-b72d-34530ae82605
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetUpdateCount, GetUpdateCount method [Windows Sync], GetUpdateCount method [Windows Sync],IFeedClockVector interface, IFeedClockVector interface [Windows Sync],GetUpdateCount method, IFeedClockVector.GetUpdateCount, IFeedClockVector::GetUpdateCount, winsync.ifeedclockvector_getupdatecount, winsync/IFeedClockVector::GetUpdateCount
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IFeedClockVector.GetUpdateCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFeedClockVector::GetUpdateCount


## -description


Gets the number of updates that have been made to the FeedSync item.


## -parameters




### -param pdwUpdateCount [out]

Returns the number of updates that have been made to the FeedSync item. This value corresponds to the <b>updates</b> attribute of the FeedSync item.


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
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9acee83e-a16c-4511-a1e3-ce653ed09535">IFeedClockVector Interface</a>
 

 

