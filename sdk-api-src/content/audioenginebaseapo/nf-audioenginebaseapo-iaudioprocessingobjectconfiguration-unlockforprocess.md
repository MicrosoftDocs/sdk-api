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

# IAudioProcessingObjectConfiguration::UnlockForProcess


## -description


The <code>UnlockForProcess</code> method releases the lock that was imposed on the APO by the LockForProcess method.


## -parameters






#### - None


## -returns



The <code>UnlockForProcess</code> method returns a value of S_OK if the call completed successfully. If the APO was already unlocked when the call was made, the method returns a value of APOERR_ALREADY_UNLOCKED.




## -remarks



The <code>UnlockForProcess</code> method places the APO in a mode that makes configuration changes possible. These changes include Add, Remove, and Swap of the input and output connections that are attached to the APO.



