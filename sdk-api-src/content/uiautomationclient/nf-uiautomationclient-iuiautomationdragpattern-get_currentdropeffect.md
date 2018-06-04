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

# IUIAutomationDragPattern::get_CurrentDropEffect


## -description


Retrieves a localized string that indicates what happens when the user drops this element as part of a drag-drop operation.  

This property is read-only.


## -parameters


## -remarks



In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="https://msdn.microsoft.com/DD5EE4A0-E6C0-4657-A60F-7F59FC569E04">DropTarget</a> pattern.  To find out what effect dropping the dragged element will have, a client can query the <a href="https://msdn.microsoft.com/90850574-83EA-4291-99D0-391D8CACFE9F">DropEffect</a> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".  The string is always localized.




## -see-also




<a href="https://msdn.microsoft.com/F7768A87-3981-48E0-A72D-BEA14C189E6E">IUIAutomationDragPattern</a>



<a href="https://msdn.microsoft.com/083B9B3C-B4B8-4336-8614-61899FBC5E47">IUIAutomationDropTargetPattern::CachedDropTargetEffect</a>



<a href="https://msdn.microsoft.com/C7A2C62B-D61B-4884-BEF0-E4EB1088D1AB">IUIAutomationDropTargetPattern::CurrentDropTargetEffect</a>



<a href="https://msdn.microsoft.com/FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE">UI Automation Support for Drag-and-Drop</a>
 

 

