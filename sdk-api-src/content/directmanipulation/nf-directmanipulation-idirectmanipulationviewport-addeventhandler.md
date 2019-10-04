---
UID: NF:directmanipulation.IDirectManipulationViewport.AddEventHandler
title: IDirectManipulationViewport::AddEventHandler (directmanipulation.h)
author: windows-sdk-content
description: Adds a new event handler to listen for viewport events.
old-location: directmanipulation\idirectmanipulationviewport_addeventhandler.htm
tech.root: directmanipulation
ms.assetid: 56b47fec-dfa2-4906-9135-5ee331f04c54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddEventHandler, AddEventHandler method [Direct Manipulation], AddEventHandler method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],AddEventHandler method, IDirectManipulationViewport.AddEventHandler, IDirectManipulationViewport::AddEventHandler, directmanipulation.idirectmanipulationviewport_addeventhandler, directmanipulation/IDirectManipulationViewport::AddEventHandler
ms.topic: method
f1_keywords: 
 - "directmanipulation/IDirectManipulationViewport.AddEventHandler"
dev_langs:
 - c++
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
 - IDirectManipulationViewport.AddEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationViewport::AddEventHandler


## -description


Adds a new event handler to listen for viewport events.


## -parameters




### -param window [in]

The handle of a window owned by the thread for the event callback.


### -param eventHandler [in]

The handler that is called when viewport status and update events occur. The specified object must implement the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewporteventhandler">IDirectManipulationViewportEventHandler</a> interface.


### -param cookie [out, retval]

The handle that represents this event handler callback.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The event callback is fired from the thread that owns the specified window. Consecutive events of the same callback method may be coalesced. 


<div class="alert"><b>Note</b>  If the viewport has a drag-drop behavior attached, the event handler should implement <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdragdropeventhandler">IDirectManipulationDragDropEventHandler</a>.
</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>
 

 

