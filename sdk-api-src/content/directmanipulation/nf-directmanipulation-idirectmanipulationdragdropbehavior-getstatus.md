---
UID: NF:directmanipulation.IDirectManipulationDragDropBehavior.GetStatus
title: IDirectManipulationDragDropBehavior::GetStatus
author: windows-sdk-content
description: Gets the status of the drag-drop interaction for the viewport this behavior is attached to.
old-location: directmanipulation\idirectmanipulationdragdropbehavior_getstatus.htm
tech.root: directmanipulation
ms.assetid: 40D706B0-E396-436C-BD0B-66B8F6EFA5B1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStatus, GetStatus method [Direct Manipulation], GetStatus method [Direct Manipulation],IDirectManipulationDragDropBehavior interface, IDirectManipulationDragDropBehavior interface [Direct Manipulation],GetStatus method, IDirectManipulationDragDropBehavior.GetStatus, IDirectManipulationDragDropBehavior::GetStatus, directmanipulation.idirectmanipulationdragdropbehavior_getstatus, directmanipulation/IDirectManipulationDragDropBehavior::GetStatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirectManipulationDragDropBehavior.GetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationDragDropBehavior::GetStatus


## -description


Gets the status of the drag-drop interaction for the viewport this behavior is attached to. 


## -parameters




### -param status [out, retval]

One of the values from <a href="https://msdn.microsoft.com/BC3B8541-E18B-4654-80C8-C5EC1359BE2F">DIRECTMANIPULATION_DRAG_DROP_STATUS</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns the drag-drop status at the time of the call and not at the time when the return value is read.




## -see-also




<a href="https://msdn.microsoft.com/99D99BB6-1DA1-4B49-88F8-16A9561A9098">IDirectManipulationDragDropBehavior</a>
 

 

