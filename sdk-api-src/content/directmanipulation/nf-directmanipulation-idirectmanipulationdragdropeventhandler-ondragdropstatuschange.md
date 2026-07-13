---
UID: NF:directmanipulation.IDirectManipulationDragDropEventHandler.OnDragDropStatusChange
title: IDirectManipulationDragDropEventHandler::OnDragDropStatusChange (directmanipulation.h)
description: Called when a status change happens in the viewport that the drag-and-drop behavior is attached to.
helpviewer_keywords: ["IDirectManipulationDragDropEventHandler interface [Direct Manipulation]","OnDragDropStatusChange method","IDirectManipulationDragDropEventHandler.OnDragDropStatusChange","IDirectManipulationDragDropEventHandler::OnDragDropStatusChange","OnDragDropStatusChange","OnDragDropStatusChange method [Direct Manipulation]","OnDragDropStatusChange method [Direct Manipulation]","IDirectManipulationDragDropEventHandler interface","directmanipulation.idirectmanipulationdragdropeventhandler_ondragdropstatuschange","directmanipulation/IDirectManipulationDragDropEventHandler::OnDragDropStatusChange"]
old-location: directmanipulation\idirectmanipulationdragdropeventhandler_ondragdropstatuschange.htm
tech.root: directmanipulation
ms.assetid: 4AC5DB55-57EF-4182-B4B9-3A4F1DE0E6B0
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDragDropEventHandler interface [Direct Manipulation],OnDragDropStatusChange method, IDirectManipulationDragDropEventHandler.OnDragDropStatusChange, IDirectManipulationDragDropEventHandler::OnDragDropStatusChange, OnDragDropStatusChange, OnDragDropStatusChange method [Direct Manipulation], OnDragDropStatusChange method [Direct Manipulation],IDirectManipulationDragDropEventHandler interface, directmanipulation.idirectmanipulationdragdropeventhandler_ondragdropstatuschange, directmanipulation/IDirectManipulationDragDropEventHandler::OnDragDropStatusChange
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationDragDropEventHandler::OnDragDropStatusChange
 - directmanipulation/IDirectManipulationDragDropEventHandler::OnDragDropStatusChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationDragDropEventHandler.OnDragDropStatusChange
---

# IDirectManipulationDragDropEventHandler::OnDragDropStatusChange


## -description

Called when a status change happens in the viewport that the drag-and-drop behavior is attached to.

## -parameters

### -param viewport [in]

The updated viewport.

### -param current [in]

The current state of the drag-drop interaction from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_drag_drop_status">DIRECTMANIPULATION_DRAG_DROP_STATUS</a>.

### -param previous [in]

The previous state of the drag-drop interaction from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_drag_drop_status">DIRECTMANIPULATION_DRAG_DROP_STATUS</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If a class  is implementing <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewporteventhandler">IDirectManipulationViewportEventHandler</a> it should also implement <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdragdropeventhandler">IDirectManipulationDragDropEventHandler</a> if that viewport will use drag and drop. <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> will query the <b>IDirectManipulationViewportEventHandler</b> instances to verify that  they also implement <b>IDirectManipulationDragDropEventHandler</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdragdropeventhandler">IDirectManipulationDragDropEventHandler</a>