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

# BatteryClassUnload function


## -description


<b>BatteryClassUnload</b> frees resources for a battery device that is no longer in use.


## -parameters




### -param ClassData [in]

Pointer to a battery class handle previously returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff536266">BatteryClassInitializeDevice</a>.


## -returns



<b>BatteryClassUnload</b> returns STATUS_SUCCESS.




## -remarks



<b>BatteryClassUnload</b> frees the battery class handle and unloads the battery device. In essence, it undoes the registration and initialization performed by <b>BatteryClassInitializeDevice</b>.

A miniclass driver should call this routine when its battery device is no longer available for use. Typically, the driver might make such a call from its Unload routine or when handling a PnP <a href="https://msdn.microsoft.com/library/windows/hardware/ff551738">IRP_MN_REMOVE_DEVICE</a> request.



