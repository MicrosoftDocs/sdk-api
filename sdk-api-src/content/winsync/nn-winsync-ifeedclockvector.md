---
UID: NN:winsync.IFeedClockVector
title: IFeedClockVector
author: windows-sdk-content
description: Represents a clock vector that contains FeedSync information.
old-location: winsync\ifeedclockvector.htm
tech.root: winsync
ms.assetid: 9acee83e-a16c-4511-a1e3-ce653ed09535
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFeedClockVector, IFeedClockVector interface [Windows Sync], IFeedClockVector interface [Windows Sync],described, winsync.ifeedclockvector, winsync/IFeedClockVector
ms.prod: windows
ms.technology: windows-sdk
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
 - IFeedClockVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFeedClockVector interface


## -description


Represents a clock vector that contains FeedSync information.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFeedClockVector</b> interface inherits from <b>IClockVector</b>. <b>IFeedClockVector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFeedClockVector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8cf6b0f-2049-4047-b72d-34530ae82605">GetUpdateCount</a>
</td>
<td align="left" width="63%">
Gets the number of updates that have been made to the FeedSync item.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d43d193b-d0c4-4b01-be90-a322fcc8b672">IsNoConflictsSpecified</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether conflicts are preserved for the FeedSync item.


</td>
</tr>
</table> 


## -see-also




<b>IClockVector</b>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

