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

# IDsAdminNotifyHandler::End


## -description


The <b>IDsAdminNotifyHandler::End</b> method is called after the notification event has occurred. This method is called even if the notification process is canceled.


## -parameters






## -returns



The return value from this method is ignored.




## -remarks



This method provides the opportunity for the notification handler to free any memory allocated during the <a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a> or <a href="https://msdn.microsoft.com/ac0b9da5-b0e3-4280-ae9c-602e28c907b1">IDsAdminNotifyHandler::Notify</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/d55e1473-8e51-441e-bd22-63208b294e14">IDsAdminNotifyHandler</a>



<a href="https://msdn.microsoft.com/443fe344-6545-45bd-8e2f-85347505d407">IDsAdminNotifyHandler::Begin</a>



<a href="https://msdn.microsoft.com/ac0b9da5-b0e3-4280-ae9c-602e28c907b1">IDsAdminNotifyHandler::Notify</a>
 

 

