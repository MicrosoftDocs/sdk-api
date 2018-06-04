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

# DdQueryDisplaySettingsUniqueness function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use 
    the Microsoft DirectDraw and Microsoft Direct3DAPIs; these 
    APIs insulate applications from such operating system changes, and hide many other 
    difficulties involved in interacting directly with display drivers.]

Returns the current value of an integer that is incremented whenever a mode switch occurs, such as when there 
    is a desktop switch, a Fast User Switch, or a full-screen Microsoft MS-DOS box. The application can call 
    this function repeatedly and compare the old and new values of the return value to determine whether display 
    settings have changed.

<b>GdiEntry13</b> is defined as an alias for this function.


## -parameters






## -returns



The current value of the mode switch integer is returned.




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

