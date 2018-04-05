---
UID: NN:comsvcs.IMessageMover
title: IMessageMover
author: windows-driver-content
description: Moves messages from one queue to another queue.
old-location: cos\imessagemover.htm
old-project: cossdk
ms.assetid: aa7c57a2-0dee-4f18-bce4-4fcc47d4d7a7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IMessageMover, IMessageMover interface [COM+], IMessageMover interface [COM+], described, _cos_IMessageMover, comsvcs/IMessageMover, cos.imessagemover
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IMessageMover
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMessageMover interface


## -description


Moves messages from one queue to another queue.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMessageMover</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMessageMover</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMessageMover</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c0b5ebb-00dc-4c9a-9c0c-6d92cd13f534">get_CommitBatchSize</a>
</td>
<td align="left" width="63%">
Retrieves the commit batch size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3adb24d5-b56d-4740-838b-d5b7571950e2">get_DestPath</a>
</td>
<td align="left" width="63%">
Retrieves the path of the destination (output) queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41fd8a17-1c9d-484c-b0f4-69f232214e48">get_SourcePath</a>
</td>
<td align="left" width="63%">
Retrieves the current path of the source (input) queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebe06730-710b-42ce-b905-be87971b19c3">MoveMessages</a>
</td>
<td align="left" width="63%">
Moves all messages from the source queue to the destination queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/107a934b-565e-444d-a042-2325b8f18754">put_CommitBatchSize</a>
</td>
<td align="left" width="63%">
Sets the commit batch size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79ed8030-097d-4017-be8e-e812f4b14a46">put_DestPath</a>
</td>
<td align="left" width="63%">
Sets the path of the destination (output) queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9807fa0-905d-452c-ba26-e59463a7fe7b">put_SourcePath</a>
</td>
<td align="left" width="63%">
Sets the path of the source (input) queue.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3a528e92-37ac-4108-b52a-557a90da4a47">IPlaybackControl</a>
 

 

