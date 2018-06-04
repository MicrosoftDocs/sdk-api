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

# IDsAdminNotifyHandler::Notify


## -description


The <b>IDsAdminNotifyHandler::Notify</b> method is called  for each object after the confirmation dialog box has been displayed and the notification handler is selected in the confirmation dialog box.


## -parameters




### -param nItem [in]

Contains the index of the item in the <b>aObjects</b> member of the <a href="https://msdn.microsoft.com/dfc1e88f-40ff-4ec1-9718-4801f678fa3f">DSOBJECTNAMES</a> structure supplied in the <a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a> method.


### -param uFlags [in]

Contains the flags supplied by the notification handler in the <a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a> method.


## -returns



The return value from this method is ignored.




## -see-also




<a href="https://msdn.microsoft.com/dfc1e88f-40ff-4ec1-9718-4801f678fa3f">DSOBJECTNAMES</a>



<a href="https://msdn.microsoft.com/d55e1473-8e51-441e-bd22-63208b294e14">IDsAdminNotifyHandler</a>



<a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a>
 

 

