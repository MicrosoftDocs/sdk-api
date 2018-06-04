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

# WscUnRegisterChanges function


## -description


Cancels a callback registration that was made by a call to the <a href="https://msdn.microsoft.com/55f2d281-6308-4344-98dc-3b1c7cbee9df">WscRegisterForChanges</a> function.


## -parameters




### -param hRegistrationHandle [in]

The handle to the registration context returned as the <i>phCallbackRegistration</i> of the <a href="https://msdn.microsoft.com/55f2d281-6308-4344-98dc-3b1c7cbee9df">WscRegisterForChanges</a> function.


## -returns



Returns <b>S_OK</b> if the function succeeds, otherwise returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/55f2d281-6308-4344-98dc-3b1c7cbee9df">WscRegisterForChanges</a>
 

 

