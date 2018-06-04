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

# FlashWindowEx function


## -description


Flashes the specified window. It does not change the active state of the window.


## -parameters




### -param pfwi [in]

A pointer to a 
<a href="https://msdn.microsoft.com/b16636bc-fa77-4eb9-9801-dc2cdf0556e5">FLASHWINFO</a> structure.


## -returns



The return value specifies the window's state before the call to the 
<b>FlashWindowEx</b> function. If the window caption was drawn as active before the call, the return value is nonzero. Otherwise, the return value is zero.




## -remarks



Typically, you flash a window to inform the user that the window requires attention but does not currently have the keyboard focus. When a window flashes, it appears to change from inactive to active status. An inactive caption bar changes to an active caption bar; an active caption bar changes to an inactive caption bar.




## -see-also




<a href="https://msdn.microsoft.com/ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5">Error Handling Functions</a>



<a href="https://msdn.microsoft.com/b16636bc-fa77-4eb9-9801-dc2cdf0556e5">FLASHWINFO</a>



<a href="https://msdn.microsoft.com/35b6e93c-323a-4592-9394-a2e9dd79d9e6">Notifying the User</a>
 

 

