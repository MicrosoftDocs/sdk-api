---
UID: NF:directmanipulation.IDirectManipulationDragDropEventHandler.OnDragDropStatusChange
title: IDirectManipulationDragDropEventHandler::OnDragDropStatusChange
author: windows-sdk-content
description: Called when a status change happens in the viewport that the drag-and-drop behavior is attached to.
old-location: directmanipulation\idirectmanipulationdragdropeventhandler_ondragdropstatuschange.htm
old-project: directmanipulation
ms.assetid: 4AC5DB55-57EF-4182-B4B9-3A4F1DE0E6B0
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationDragDropEventHandler interface [Direct Manipulation],OnDragDropStatusChange method, IDirectManipulationDragDropEventHandler.OnDragDropStatusChange, IDirectManipulationDragDropEventHandler::OnDragDropStatusChange, OnDragDropStatusChange, OnDragDropStatusChange method [Direct Manipulation], OnDragDropStatusChange method [Direct Manipulation],IDirectManipulationDragDropEventHandler interface, directmanipulation.idirectmanipulationdragdropeventhandler_ondragdropstatuschange, directmanipulation/IDirectManipulationDragDropEventHandler::OnDragDropStatusChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationDragDropEventHandler.OnDragDropStatusChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

