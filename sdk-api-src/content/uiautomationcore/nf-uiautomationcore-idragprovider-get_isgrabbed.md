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

# IDragProvider::get_IsGrabbed


## -description


Indicates whether the element has been grabbed as part of a drag-and-drop operation.

This property is read-only.


## -parameters


## -remarks



If this property changes, the provider must notify clients by calling <a href="https://msdn.microsoft.com/ec9da198-eb1d-4883-9b5c-539c92bd530b">UiaRaiseAutomationPropertyChangedEvent</a> and specifying a property identifier of <a href="uiauto_control_pattern_propids.htm">UIA_DragIsGrabbedPropertyId</a> or <a href="uiauto_control_pattern_propids.htm">UIA_DragDropEffectPropertyId</a>.




## -see-also




<a href="https://msdn.microsoft.com/FAC4A56D-17BC-42E6-A03E-EE45D717DE37">IDragProvider</a>
 

 

