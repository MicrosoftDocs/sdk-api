---
UID: NF:directmanipulation.IDirectManipulationDragDropBehavior.GetStatus
title: IDirectManipulationDragDropBehavior::GetStatus (directmanipulation.h)
description: Gets the status of the drag-drop interaction for the viewport this behavior is attached to.
helpviewer_keywords: ["GetStatus","GetStatus method [Direct Manipulation]","GetStatus method [Direct Manipulation]","IDirectManipulationDragDropBehavior interface","IDirectManipulationDragDropBehavior interface [Direct Manipulation]","GetStatus method","IDirectManipulationDragDropBehavior.GetStatus","IDirectManipulationDragDropBehavior::GetStatus","directmanipulation.idirectmanipulationdragdropbehavior_getstatus","directmanipulation/IDirectManipulationDragDropBehavior::GetStatus"]
old-location: directmanipulation\idirectmanipulationdragdropbehavior_getstatus.htm
tech.root: directmanipulation
ms.assetid: 40D706B0-E396-436C-BD0B-66B8F6EFA5B1
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Direct Manipulation], GetStatus method [Direct Manipulation],IDirectManipulationDragDropBehavior interface, IDirectManipulationDragDropBehavior interface [Direct Manipulation],GetStatus method, IDirectManipulationDragDropBehavior.GetStatus, IDirectManipulationDragDropBehavior::GetStatus, directmanipulation.idirectmanipulationdragdropbehavior_getstatus, directmanipulation/IDirectManipulationDragDropBehavior::GetStatus
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
 - IDirectManipulationDragDropBehavior::GetStatus
 - directmanipulation/IDirectManipulationDragDropBehavior::GetStatus
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
 - IDirectManipulationDragDropBehavior.GetStatus
---

# IDirectManipulationDragDropBehavior::GetStatus


## -description

Gets the status of the drag-drop interaction for the viewport this behavior is attached to.

## -parameters

### -param status [out, retval]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_drag_drop_status">DIRECTMANIPULATION_DRAG_DROP_STATUS</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns the drag-drop status at the time of the call and not at the time when the return value is read.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdragdropbehavior">IDirectManipulationDragDropBehavior</a>