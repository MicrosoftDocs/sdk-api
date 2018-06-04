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

# MCIWndRegisterClass function


## -description



The <b>MCIWndRegisterClass</b> function registers the MCI window class MCIWND_WINDOW_CLASS.




## -parameters






#### - hInstance

Handle to the device instance.


## -returns



Returns zero if successful.




## -remarks



After registering the MCI window class, use the <b>CreateWindow</b> or <b>CreateWindowEx</b> functions to create an MCIWnd window. If your application uses this function, it does not need to use the <a href="https://msdn.microsoft.com/7a4a22e1-6b04-4d46-8427-738181769f5b">MCIWndCreate</a> function.



