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

# GetThreadDpiHostingBehavior function


## -description


Retrieves the <a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> from the current thread.


## -parameters






## -returns



The <a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the current thread.




## -remarks



This API returns the hosting behavior set by an earlier call of  <a href="hidpi.setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>, or <b>DPI_HOSTING_BEHAVIOR_DEFAULT</b> if no earlier call has been made.




## -see-also




<a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a>



<a href="hidpi.getwindowdpihostingbehavior">GetWindowDpiHostingBehavior</a>



<a href="hidpi.setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>
 

 

