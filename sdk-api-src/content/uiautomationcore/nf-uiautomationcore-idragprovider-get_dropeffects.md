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

# IDragProvider::get_DropEffects


## -description


Retrieves an array of localized strings that enumerate the  full set of effects that can happen when this element is dropped as part of a drag-and-drop operation.

This property is read-only.


## -parameters


## -remarks



Some drag operations support a set of different drop effects. For example, a drag operation initiated through a right-click might display a menu of options when the element is dropped.   In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="https://msdn.microsoft.com/DD5EE4A0-E6C0-4657-A60F-7F59FC569E04">DropTarget</a> pattern.    To find out what effect dropping the dragged element will have, a client can query the <a href="https://msdn.microsoft.com/90850574-83EA-4291-99D0-391D8CACFE9F">DropEffect</a> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".    The strings are always localized.




## -see-also




<a href="https://msdn.microsoft.com/FAC4A56D-17BC-42E6-A03E-EE45D717DE37">IDragProvider</a>
 

 

