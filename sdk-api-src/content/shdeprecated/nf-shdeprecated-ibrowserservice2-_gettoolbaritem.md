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

# IBrowserService2::_GetToolbarItem


## -description


Deprecated. Gets a specific item from a toolbar.


## -parameters




### -param itb [in]

Type: <b>int</b>

The index of the toolbar item to retrieve.


## -returns



Type: <b>LPTOOLBARITEM</b>

A pointer to a <a href="https://msdn.microsoft.com/7378f2f3-c164-46fe-9989-a7a57fceb48a">TOOLBARITEM</a> structure that represents a toolbar item.




## -remarks



This method is implemented by the derived class.



