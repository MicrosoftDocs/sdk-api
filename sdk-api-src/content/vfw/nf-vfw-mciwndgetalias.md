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

# MCIWndGetAlias macro


## -description



The <b>MCIWndGetAlias</b> macro retrieves the alias used to open an MCI device or file with the <a href="https://msdn.microsoft.com/e751da38-a586-43d6-9c21-a4b6b5860a33">mciSendString</a> function. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/37131b89-275c-4ab6-9278-0e08c42471bd">MCIWNDM_GETALIAS</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -see-also




<a href="https://msdn.microsoft.com/37131b89-275c-4ab6-9278-0e08c42471bd">MCIWNDM_GETALIAS</a>
 

 

