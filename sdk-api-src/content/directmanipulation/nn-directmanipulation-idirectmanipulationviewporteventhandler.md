---
UID: NN:directmanipulation.IDirectManipulationViewportEventHandler
title: IDirectManipulationViewportEventHandler
author: windows-sdk-content
description: Defines methods for handling status and update events for the viewport.
old-location: directmanipulation\idirectmanipulationviewporteventhandler.htm
tech.root: directmanipulation
ms.assetid: 3594011a-da4a-4550-9b3b-076218d09f39
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectManipulationViewportEventHandler, IDirectManipulationViewportEventHandler interface [Direct Manipulation], IDirectManipulationViewportEventHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationviewporteventhandler, directmanipulation/IDirectManipulationViewportEventHandler
ms.topic: interface
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IDirectManipulationViewportEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewportEventHandler interface


## -description



Defines methods for handling status and update events for the viewport.


<div class="alert"><b>Note</b>  When implementing a <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> object, ensure that the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms683614(v=VS.85).aspx">InterlockedIncrement</a> and <a href="https://msdn.microsoft.com/en-us/library/ms683580(v=VS.85).aspx">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationViewportEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationViewportEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationViewportEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b9a0f54-ccc7-4927-a34e-724652f6c2f0">OnContentUpdated</a>
</td>
<td align="left" width="63%">
Called when content inside a viewport is updated.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fe7106d-1b13-4a3e-8841-550e0ef55f95">OnViewportStatusChanged</a>
</td>
<td align="left" width="63%">
Called when the status of a viewport changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfb70d6f-ce3c-4d39-b7b5-21812ff7e56b">OnViewportUpdated</a>
</td>
<td align="left" width="63%">
Called after all content in the viewport has been updated.

</td>
</tr>
</table> 


## -remarks



Client apps implement this handler to receive status and update events for viewports. Use <a href="https://msdn.microsoft.com/56b47fec-dfa2-4906-9135-5ee331f04c54">AddEventHandler</a> to set the handler for a viewport. Each viewport can have more than one handler.




## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

