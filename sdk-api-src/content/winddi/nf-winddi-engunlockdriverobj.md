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

# EngUnlockDriverObj function


## -description


The <b>EngUnlockDriverObj</b> function causes GDI to unlock the driver object.


## -parameters




### -param hdo

Identifies the object to be unlocked.


## -returns



The return value is <b>TRUE</b> if the function is successful; otherwise, it is <b>FALSE</b>.




## -remarks



The specified driver object must have been previously locked by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564967">EngLockDriverObj</a>. The object is not unlockable by another thread while it is locked down.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564967">EngLockDriverObj</a>
 

 

