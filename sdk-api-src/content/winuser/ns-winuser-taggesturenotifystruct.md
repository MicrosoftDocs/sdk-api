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

# tagGESTURENOTIFYSTRUCT structure


## -description



      When transmitted with <a href="https://msdn.microsoft.com/83c23928-86ce-421d-bb84-5c41a770bf60">WM_GESTURENOTIFY</a> messages, 
      passes information about a gesture.
  


## -struct-fields




### -field cbSize

The size of the structure.


### -field dwFlags

Reserved for future use.


### -field hwndTarget

The target window for the gesture notification.


### -field ptsLocation

The location of the gesture in physical screen coordinates.


### -field dwInstanceID

A specific gesture instance with gesture messages starting with <b>GID_START</b> and ending with <b>GID_END</b>.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>



<a href="https://msdn.microsoft.com/83c23928-86ce-421d-bb84-5c41a770bf60">WM_GESTURENOTIFY</a>
 

 

