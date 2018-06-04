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

# IInkOverlay::get_SupportHighContrastSelectionUI


## -description



Gets or sets a value that specifies whether all selection user interface (UI) elements are drawn in high contrast when the system is in High Contrast mode.



This property is read/write.


## -parameters


## -remarks



This property changes the way selection UI is displayed when the system changes to High Contrast mode. Selection UI elements include the selection bounding box and the selection handles.

Ink selection uses the COLOR_WINDOWTEXT, COLOR_WINDOW, and COLOR_HIGHLIGHT system colors to draw elements of the selection UI when the system is in High Contrast mode and the <b>SupportHighContrastSelectionUI</b> property is <b>TRUE</b>. For more information on system colors, see the <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> function in MSDN.




## -see-also




<a href="https://msdn.microsoft.com/885ace6d-952e-4870-b92c-92e47daadfcf">Color Property</a>



<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/17f5002b-0191-4cb0-8b12-0383aaabe2a8">SupportHighContrastInk Property</a>
 

 

