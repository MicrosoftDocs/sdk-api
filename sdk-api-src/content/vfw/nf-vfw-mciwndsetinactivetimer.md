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

# MCIWndSetInactiveTimer macro


## -description



The <b>MCIWndSetInactiveTimer</b> macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/8900c372-0493-4a63-a027-ef6ecf8f8254">MCIWNDM_SETINACTIVETIMER</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param inactive

Update period, in milliseconds. The default is 2000 milliseconds. 

