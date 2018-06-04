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

# IDirectManipulationDragDropEventHandler::OnDragDropStatusChange


## -description


Called when a status change happens in the viewport that the drag-and-drop behavior is attached to. 


## -parameters




### -param viewport [in]

The updated viewport.


### -param current [in]

The current state of the drag-drop interaction from <a href="https://msdn.microsoft.com/BC3B8541-E18B-4654-80C8-C5EC1359BE2F">DIRECTMANIPULATION_DRAG_DROP_STATUS</a>. 


### -param previous [in]

The previous state of the drag-drop interaction from <a href="https://msdn.microsoft.com/BC3B8541-E18B-4654-80C8-C5EC1359BE2F">DIRECTMANIPULATION_DRAG_DROP_STATUS</a>. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If a class  is implementing <a href="https://msdn.microsoft.com/3594011a-da4a-4550-9b3b-076218d09f39">IDirectManipulationViewportEventHandler</a> it should also implement <a href="https://msdn.microsoft.com/B0F4120F-E64C-4224-A1C5-00DBEE63949B">IDirectManipulationDragDropEventHandler</a> if that viewport will use drag and drop. <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> will query the <b>IDirectManipulationViewportEventHandler</b> instances to verify that  they also implement <b>IDirectManipulationDragDropEventHandler</b>.





## -see-also




<a href="https://msdn.microsoft.com/B0F4120F-E64C-4224-A1C5-00DBEE63949B">IDirectManipulationDragDropEventHandler</a>
 

 

