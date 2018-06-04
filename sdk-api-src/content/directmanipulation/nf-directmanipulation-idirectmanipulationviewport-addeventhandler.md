---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDirectManipulationViewport::AddEventHandler


## -description


Adds a new event handler to listen for viewport events.


## -parameters




### -param window [in]

The handle of a window owned by the thread for the event callback.


### -param eventHandler [in]

The handler that is called when viewport status and update events occur. The specified object must implement the <a href="https://msdn.microsoft.com/3594011a-da4a-4550-9b3b-076218d09f39">IDirectManipulationViewportEventHandler</a> interface.


### -param cookie [out, retval]

The handle that represents this event handler callback.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The event callback is fired from the thread that owns the specified window. Consecutive events of the same callback method may be coalesced. 


<div class="alert"><b>Note</b>  If the viewport has a drag-drop behavior attached, the event handler should implement <a href="https://msdn.microsoft.com/B0F4120F-E64C-4224-A1C5-00DBEE63949B">IDirectManipulationDragDropEventHandler</a>.
</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

