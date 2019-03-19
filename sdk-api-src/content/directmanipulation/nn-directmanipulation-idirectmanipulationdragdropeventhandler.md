---
UID: NN:directmanipulation.IDirectManipulationDragDropEventHandler
title: IDirectManipulationDragDropEventHandler (directmanipulation.h)
author: windows-sdk-content
description: Defines methods to handle drag-drop behavior events.
old-location: directmanipulation\idirectmanipulationdragdropeventhandler.htm
tech.root: directmanipulation
ms.assetid: B0F4120F-E64C-4224-A1C5-00DBEE63949B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectManipulationDragDropEventHandler, IDirectManipulationDragDropEventHandler interface [Direct Manipulation], IDirectManipulationDragDropEventHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdragdropeventhandler, directmanipulation/IDirectManipulationDragDropEventHandler
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
 - IDirectManipulationDragDropEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationDragDropEventHandler interface


## -description


Defines methods to handle drag-drop behavior events.
<div class="alert"><b>Note</b>  When implementing this interface, ensure that the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms683614(v=VS.85).aspx">InterlockedIncrement</a> and <a href="https://msdn.microsoft.com/en-us/library/ms683580(v=VS.85).aspx">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationDragDropEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationDragDropEventHandler</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4AC5DB55-57EF-4182-B4B9-3A4F1DE0E6B0">OnDragDropStatusChange</a>
</td>
<td align="left" width="63%">
Called when a status change happens in the viewport that the drag-and-drop behavior is attached to. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

