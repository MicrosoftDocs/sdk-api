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

# GetWindowDpiHostingBehavior function


## -description


Returns the <a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the specified window.


## -parameters




### -param hwnd

The handle for the window to examine.


## -returns



The <a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the specified window.




## -remarks



This API allows you to examine the hosting behavior of a window after it has been created. A window's hosting behavior is the hosting behavior of the thread in which the window was created, as set by a call to <a href="hidpi.setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>. This is a permanent value and cannot be changed after the window is created, even if the thread's hosting behavior is changed.




## -see-also




<a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a>



<a href="hidpi.getthreaddpihostingbehavior">GetThreadDpiHostingBehavior</a>



<a href="hidpi.setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>
 

 

