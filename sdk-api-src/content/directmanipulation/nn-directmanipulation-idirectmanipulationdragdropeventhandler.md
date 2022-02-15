---
UID: NN:directmanipulation.IDirectManipulationDragDropEventHandler
title: IDirectManipulationDragDropEventHandler (directmanipulation.h)
description: Defines methods to handle drag-drop behavior events.
helpviewer_keywords: ["IDirectManipulationDragDropEventHandler","IDirectManipulationDragDropEventHandler interface [Direct Manipulation]","IDirectManipulationDragDropEventHandler interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationdragdropeventhandler","directmanipulation/IDirectManipulationDragDropEventHandler"]
old-location: directmanipulation\idirectmanipulationdragdropeventhandler.htm
tech.root: directmanipulation
ms.assetid: B0F4120F-E64C-4224-A1C5-00DBEE63949B
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDragDropEventHandler, IDirectManipulationDragDropEventHandler interface [Direct Manipulation], IDirectManipulationDragDropEventHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdragdropeventhandler, directmanipulation/IDirectManipulationDragDropEventHandler
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
 - IDirectManipulationDragDropEventHandler
 - directmanipulation/IDirectManipulationDragDropEventHandler
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
 - IDirectManipulationDragDropEventHandler
---

# IDirectManipulationDragDropEventHandler interface


## -description

Defines methods to handle drag-drop behavior events.
<div class="alert"><b>Note</b>  When implementing this interface, ensure that the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a> and <a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b>IDirectManipulationDragDropEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationDragDropEventHandler</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
