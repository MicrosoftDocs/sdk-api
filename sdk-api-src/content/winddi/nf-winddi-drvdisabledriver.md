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

# DrvDisableDriver function


## -description


The <b>DrvDisableDriver</b> function is used by GDI to notify a driver that it no longer requires the driver and is ready to unload it.


## -parameters






## -returns



None




## -remarks



The driver should free all allocated resources and return the device to the state it was in before the driver was loaded.

<b>DrvDisableDriver</b> is required for graphics drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556210">DrvEnableDriver</a>
 

 

