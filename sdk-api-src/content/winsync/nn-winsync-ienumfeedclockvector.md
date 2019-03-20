---
UID: NN:winsync.IEnumFeedClockVector
title: IEnumFeedClockVector (winsync.h)
author: windows-sdk-content
description: Enumerates the clock vector elements that are stored in a clock vector that contains FeedSync information.
old-location: winsync\ienumfeedclockvector.htm
tech.root: winsync
ms.assetid: 87679327-3a09-4416-b802-91171feb160a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumFeedClockVector, IEnumFeedClockVector interface [Windows Sync], IEnumFeedClockVector interface [Windows Sync],described, winsync.ienumfeedclockvector, winsync/IEnumFeedClockVector
ms.topic: interface
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
 - IEnumFeedClockVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumFeedClockVector interface


## -description


Enumerates the clock vector elements that are stored in a clock vector that contains FeedSync information.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumFeedClockVector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumFeedClockVector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumFeedClockVector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad2664d2-c36c-46bf-9f80-001c2e5d4251">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2303fac8-21ae-44df-8e47-9fe0fa88d90b">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the clock vector, if available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbd25148-b734-49a2-b8ad-9ded9d1a0bf2">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the clock vector.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eabe3389-2c1f-4b0e-a062-24bbe3fa87f9">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of clock vector elements.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

