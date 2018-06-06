---
UID: NN:winsync.ISyncCallback
title: ISyncCallback
author: windows-sdk-content
description: Represents application callbacks that are used to notify the application of synchronization events.
old-location: winsync\isynccallback.htm
old-project: winsync
ms.assetid: f6c96e02-e9db-402c-8197-580f688b068f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncCallback, ISyncCallback interface [Windows Sync], ISyncCallback interface [Windows Sync],described, winsync.isynccallback, winsync/ISyncCallback
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncCallback interface


## -description


Represents application callbacks that are used to notify the application of synchronization events.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16bcc448-8acc-4349-a5d1-0c0764afe2ec">OnChange</a>
</td>
<td align="left" width="63%">
Occurs before a change is applied.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/439f2a73-b36c-4604-b739-9f9b68275ac5">OnConflict</a>
</td>
<td align="left" width="63%">
Occurs when a conflict is detected when the concurrency conflict resolution policy is set to <a href="https://msdn.microsoft.com/4c2f7237-32ac-4f2d-bf6a-7959bc5d40d4">CRP_NONE</a>.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f52ddaf2-9ce2-4ebb-bace-024c059b2594">OnFullEnumerationNeeded</a>
</td>
<td align="left" width="63%">
Occurs when the forgotten knowledge from the source provider is not contained in the current knowledge of the destination provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a4dad07-b169-4767-a118-3b5c6c8b9764">OnProgress</a>
</td>
<td align="left" width="63%">
Occurs periodically during the synchronization session to report progress.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de496e83-cfa4-47c7-9b07-712e59737532">OnRecoverableError</a>
</td>
<td align="left" width="63%">
Occurs when a synchronization provider sets a recoverable error while it is loading or saving an item.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4c2f7237-32ac-4f2d-bf6a-7959bc5d40d4">CONFLICT_RESOLUTION_POLICY Enumeration</a>



<a href="https://msdn.microsoft.com/fea7e7f6-1570-4c34-a97c-90cd57c5acdc">Windows Sync Reference</a>
 

 

