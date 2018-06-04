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

# GetMenuContextHelpId function


## -description


Retrieves the Help context identifier associated with the specified menu.


## -parameters




### -param Arg1

TBD




#### - hmenu

Type: <b>HMENU</b>

A handle to the menu for which the Help context identifier is to be retrieved.


## -returns



Type: <b>DWORD</b>

Returns the Help context identifier if the menu has one, or zero otherwise.




## -see-also




<a href="https://msdn.microsoft.com/55d944db-d889-468a-991a-b9779c90b44f">SetMenuContextHelpId</a>
 

 

