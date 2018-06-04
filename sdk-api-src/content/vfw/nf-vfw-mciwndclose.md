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

# MCIWndClose macro


## -description



The <b>MCIWndClose</b> macro closes an MCI device or file associated with an MCIWnd window. Although the MCI device closes, the MCIWnd window is still open and can be associated with another MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f">MCI_CLOSE</a> command.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -see-also




<a href="https://msdn.microsoft.com/62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f">MCI_CLOSE</a>
 

 

