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

# _TBINFO structure


## -description


Used with the <a href="https://msdn.microsoft.com/983652ed-7309-46aa-a6c9-7516411ba5ac">SFVM_GETBUTTONINFO</a> notification to specify the number of buttons to add to the toolbar, as well as how they're added.


## -struct-fields




### -field cbuttons

Type: <b>UINT</b>

The number of buttons.


### -field uFlags

Type: <b>UINT</b>

One of the following flags.



#### TBIF_APPEND (0)

Add the new buttons after the existing buttons.



#### TBIF_PREPEND (1)

Add the new buttons before the existing buttons.



#### TBIF_REPLACE (2)

Replace the existing buttons with the new buttons.

