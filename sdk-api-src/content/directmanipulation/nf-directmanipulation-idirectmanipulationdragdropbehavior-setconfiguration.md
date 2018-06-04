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

# IDirectManipulationDragDropBehavior::SetConfiguration


## -description


Sets the configuration of the drag-drop interaction for the viewport this behavior is attached to. 


## -parameters




### -param configuration [in]

Combination  of values from <a href="https://msdn.microsoft.com/F41BD870-002B-4627-85EA-8064B156611D">DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION</a>.

For the configuration to be valid, <i>configuration</i> must contain exactly one of the following three values:
<ul>
<li><b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY</b></li>
<li><b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG</b></li>
<li><b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG</b></li>
</ul>


If <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY</b> or  <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG</b> is specified, one of <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL</b> or <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL</b> is required.


If <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG</b> is specified, both <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL</b> and <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL</b> are required.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The configuration of the behavior can be set before or after it has been added to a viewport. If a configuration change is made while an interaction is occurring, the new configuration takes effect on the next interaction.

 



<a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">IDirectManipulationViewport::ActivateConfiguration</a> should not be called prior to calling <b>IDirectManipulationDragDropBehavior::SetConfiguration</b>. This will result in  unexpected behavior.




## -see-also




<a href="https://msdn.microsoft.com/99D99BB6-1DA1-4B49-88F8-16A9561A9098">IDirectManipulationDragDropBehavior</a>



<a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">IDirectManipulationViewport::ActivateConfiguration</a>
 

 

