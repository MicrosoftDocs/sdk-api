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

# EngMapEvent function


## -description


The <b>EngMapEvent</b> function maps a user-mode event object to kernel mode.


## -parameters




### -param hDev [in]

Handle to the physical device associated with the event. This is the GDI handle passed as the <i>hdev</i> parameter to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a> function.


### -param hUserObject [in]

Handle to the user-mode event to be mapped.


### -param Reserved1

Is reserved for system use, and must be set to <b>NULL</b>.


### -param Reserved2

Is reserved for system use, and must be set to <b>NULL</b>.


### -param Reserved3

Is reserved for system use, and must be set to <b>NULL</b>.


## -returns



<b>EngMapEvent</b> returns a pointer to an event object on success. Otherwise, it returns <b>NULL</b>.




## -remarks



After successfully mapping the user event, <b>EngMapEvent</b> automatically sets the event object to the signaled state, attempts to satisfy as many waits as possible, and then resets the event object to the nonsignaled state.

A mapped event provides a mechanism by which an application can wait for a kernel-mode graphics operation to complete. The display driver or video miniport driver signals the application when it is done using the resource for which the event was mapped, thus freeing the application to use the resource.

Display and miniport drivers cannot wait for mapped events, but can set or clear them.

The driver can also perform its own cleanup by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff565434">EngUnmapEvent</a> on the event object returned by <b>EngMapEvent</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565434">EngUnmapEvent</a>
 

 

