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

# IUIAutomationTransformPattern::Resize


## -description


Resizes the UI Automation element.


## -parameters




### -param width [in]

Type: <b>double</b>

The new width of the window, in pixels.


### -param height [in]

Type: <b>double</b>

The new height of the window, in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When called on a control that supports split panes, this method can have the side effect of resizing other contiguous panes. 

An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and inaccessible to the keyboard or mouse. For example, when a top-level window is moved completely off-screen or a child object is moved outside the boundaries of the container's viewport. In these cases the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.




## -see-also




<a href="https://msdn.microsoft.com/2059daae-af25-4226-9a4d-a63e75c9ad14">CachedCanResize</a>



<a href="https://msdn.microsoft.com/2ad057b2-d382-45e0-be98-3897e5f31668">CurrentCanResize</a>



<a href="https://msdn.microsoft.com/276b44d9-a335-4d4e-8fe9-de03584dadb4">IUIAutomationTransformPattern</a>
 

 

