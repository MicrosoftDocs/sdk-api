---
UID: NN:directmanipulation.IDirectManipulationDragDropBehavior
title: IDirectManipulationDragDropBehavior (directmanipulation.h)
author: windows-sdk-content
description: Represents behaviors for drag and drop interactions, which are triggered by cross-slide or press-and-hold gestures.
old-location: directmanipulation\idirectmanipulationdragdropbehavior.htm
tech.root: directmanipulation
ms.assetid: 99D99BB6-1DA1-4B49-88F8-16A9561A9098
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDragDropBehavior, IDirectManipulationDragDropBehavior interface [Direct Manipulation], IDirectManipulationDragDropBehavior interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdragdropbehavior, directmanipulation/IDirectManipulationDragDropBehavior
ms.topic: interface
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationDragDropBehavior
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationDragDropBehavior interface


## -description


Represents behaviors for drag and drop interactions, which are triggered by cross-slide or press-and-hold gestures. 

Call <a href="https://msdn.microsoft.com/E65CF2A3-EF44-4B4E-A8C5-7DC75345B5A6">AddBehavior</a> to apply the behavior on a viewport and <a href="https://msdn.microsoft.com/CA5FF0FC-6ED9-4964-9751-90387650A198">RemoveBehavior</a> to remove it.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationDragDropBehavior</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationDragDropBehavior</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationDragDropBehavior</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40D706B0-E396-436C-BD0B-66B8F6EFA5B1">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the drag-drop interaction for the viewport this behavior is attached to. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/972EF04E-B14C-4EF9-B40A-EAF0458F2947">SetConfiguration</a>
</td>
<td align="left" width="63%">
Sets the configuration of the drag-drop interaction for the viewport this behavior is attached to. 

</td>
</tr>
</table> 


## -remarks



If <a href="https://msdn.microsoft.com/908f67ef-3606-4636-88aa-4e95d80a9c7a">AddConfiguration</a>, <a href="https://msdn.microsoft.com/2aac9468-a060-4f06-9e8e-139355be75f7">RemoveConfiguration</a>, <a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">ActivateConfiguration</a>, or <a href="https://msdn.microsoft.com/EBBBCEDB-8BAC-4E87-A69C-9730865A257F">SetManualGesture</a> has been called successfully on a viewport, <a href="https://msdn.microsoft.com/E65CF2A3-EF44-4B4E-A8C5-7DC75345B5A6">AddBehavior</a> fails for the remaining lifetime of the viewport. 

Once the behavior is added to the viewport, calls to <a href="https://msdn.microsoft.com/908f67ef-3606-4636-88aa-4e95d80a9c7a">AddConfiguration</a>, <a href="https://msdn.microsoft.com/2aac9468-a060-4f06-9e8e-139355be75f7">RemoveConfiguration</a>, <a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">ActivateConfiguration</a>, or <a href="https://msdn.microsoft.com/EBBBCEDB-8BAC-4E87-A69C-9730865A257F">SetManualGesture</a> will fail until <a href="https://msdn.microsoft.com/CA5FF0FC-6ED9-4964-9751-90387650A198">RemoveBehavior</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

