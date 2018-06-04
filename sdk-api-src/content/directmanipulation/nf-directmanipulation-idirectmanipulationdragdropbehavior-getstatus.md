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
 

 

