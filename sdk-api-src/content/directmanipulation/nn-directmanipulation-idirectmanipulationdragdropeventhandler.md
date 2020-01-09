---
UID: NN:directmanipulation.IDirectManipulationDragDropEventHandler
title: IDirectManipulationDragDropEventHandler (directmanipulation.h)
description: Defines methods to handle drag-drop behavior events.
old-location: directmanipulation\idirectmanipulationdragdropeventhandler.htm
tech.root: directmanipulation
ms.assetid: B0F4120F-E64C-4224-A1C5-00DBEE63949B
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDragDropEventHandler, IDirectManipulationDragDropEventHandler interface [Direct Manipulation], IDirectManipulationDragDropEventHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdragdropeventhandler, directmanipulation/IDirectManipulationDragDropEventHandler
ms.topic: interface
f1_keywords:
- directmanipulation/IDirectManipulationDragDropEventHandler
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
- IDirectManipulationDragDropEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationDragDropEventHandler interface


## -description


Defines methods to handle drag-drop behavior events.
<div class="alert"><b>Note</b>  When implementing this interface, ensure that the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a> and <a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationDragDropEventHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationDragDropEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationDragDropEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdragdropeventhandler-ondragdropstatuschange">OnDragDropStatusChange</a>
</td>
<td align="left" width="63%">
Called when a status change happens in the viewport that the drag-and-drop behavior is attached to. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

