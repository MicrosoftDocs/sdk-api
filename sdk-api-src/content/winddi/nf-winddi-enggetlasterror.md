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

# EngGetLastError function


## -description


The <b>EngGetLastError</b> function returns the last error code logged by GDI for the calling thread.


## -parameters






## -returns



The return value is the last error code set by <b>EngSetLastError</b>.




## -remarks



<b>EngGetLastError</b> facilitates communication of GDI and/or driver error conditions to an application.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565015">EngSetLastError</a>
 

 

