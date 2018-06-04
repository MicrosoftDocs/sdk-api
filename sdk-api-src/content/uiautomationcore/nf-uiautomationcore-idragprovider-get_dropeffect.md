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

# IDragProvider::get_DropEffect


## -description


Retrieves a localized string that indicates what happens when this element is dropped as part of a drag-drop operation.

This property is read-only.


## -parameters


## -remarks



In the source-only style of UI Automation drag-and-drop, no elements implement the <a href="https://msdn.microsoft.com/DD5EE4A0-E6C0-4657-A60F-7F59FC569E04">DropTarget</a> pattern.  To find out what effect dropping the dragged element will have, a client can query the <b>DropEffect</b> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".  The string is always localized.

If this property changes, the provider must notify clients by calling <a href="https://msdn.microsoft.com/ec9da198-eb1d-4883-9b5c-539c92bd530b">UiaRaiseAutomationPropertyChangedEvent</a> and specifying a property identifier of <a href="uiauto_control_pattern_propids.htm">UIA_DragIsGrabbedPropertyId</a> or <a href="uiauto_control_pattern_propids.htm">UIA_DragDropEffectPropertyId</a>.




## -see-also




<a href="https://msdn.microsoft.com/FAC4A56D-17BC-42E6-A03E-EE45D717DE37">IDragProvider</a>
 

 

