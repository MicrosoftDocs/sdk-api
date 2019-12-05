---
UID: NN:directmanipulation.IDirectManipulationDragDropBehavior
title: IDirectManipulationDragDropBehavior (directmanipulation.h)
description: Represents behaviors for drag and drop interactions, which are triggered by cross-slide or press-and-hold gestures.
old-location: directmanipulation\idirectmanipulationdragdropbehavior.htm
tech.root: directmanipulation
ms.assetid: 99D99BB6-1DA1-4B49-88F8-16A9561A9098
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDragDropBehavior, IDirectManipulationDragDropBehavior interface [Direct Manipulation], IDirectManipulationDragDropBehavior interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdragdropbehavior, directmanipulation/IDirectManipulationDragDropBehavior
ms.topic: interface
f1_keywords:
- directmanipulation/IDirectManipulationDragDropBehavior
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationDragDropBehavior interface


## -description


Represents behaviors for drag and drop interactions, which are triggered by cross-slide or press-and-hold gestures. 

Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-addbehavior">AddBehavior</a> to apply the behavior on a viewport and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-removebehavior">RemoveBehavior</a> to remove it.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationDragDropBehavior</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationDragDropBehavior</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdragdropbehavior-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the drag-drop interaction for the viewport this behavior is attached to. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdragdropbehavior-setconfiguration">SetConfiguration</a>
</td>
<td align="left" width="63%">
Sets the configuration of the drag-drop interaction for the viewport this behavior is attached to. 

</td>
</tr>
</table> 


## -remarks



If <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeconfiguration">RemoveConfiguration</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>, or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setmanualgesture">SetManualGesture</a> has been called successfully on a viewport, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-addbehavior">AddBehavior</a> fails for the remaining lifetime of the viewport. 

Once the behavior is added to the viewport, calls to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeconfiguration">RemoveConfiguration</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>, or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setmanualgesture">SetManualGesture</a> will fail until <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-removebehavior">RemoveBehavior</a> is called.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

