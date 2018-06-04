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

# DAD_ShowDragImage function


## -description


<p class="CCE_Message">[<b>DAD_ShowDragImage</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://msdn.microsoft.com/b4e4c1c0-21b4-4eb0-b38e-375eb5195816">ImageList_DragShowNolock</a> instead.
      ]

Shows or hides the image being dragged.


## -parameters




### -param fShow

Type: <b>BOOL</b>

A value that specifies whether to show or hide the image being dragged.



#### FALSE

Hides the image.



#### TRUE

Shows the image.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.




## -remarks



This function works on locked windows. It does not work on layered windows.



