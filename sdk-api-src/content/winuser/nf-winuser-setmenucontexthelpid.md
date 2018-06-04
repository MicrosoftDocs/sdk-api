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

# SetMenuContextHelpId function


## -description


Associates a Help context identifier with a menu.


## -parameters




### -param

TBD




#### - dwContextHelpId

Type: <b>DWORD</b>

The help context identifier.


#### - hmenu

Type: <b>HMENU</b>

A handle to the menu with which to associate the Help context identifier.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.

To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All items in the menu share this identifier. Help context identifiers can't be attached to individual menu items.




## -see-also




<a href="https://msdn.microsoft.com/2b8d3e94-6860-4a75-8373-38afb641eb3b">GetMenuContextHelpId</a>
 

 

