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

# DwmSetDxFrameDuration function


## -description


Sets the number of monitor refreshes through which to display the presented frame.
        
            

<b>DwmSetDxFrameDuration</b> is no longer supported. Starting with Windows 8.1, calls to <b>DwmSetDxFrameDuration</b> always return E_NOTIMPL.


## -parameters




### -param hwnd

The handle to the window that displays the presented frame.


### -param cRefreshes

The number of refreshes through which to display the presented frame.


## -returns



This function always returns S_OK, even when the frame duration is not changed or DWM is not running.




## -remarks



The DWM will attempt to display the presented frame for at least the number of monitor refreshes specified. It might be impossible to display the frame for the precise number of refreshes due to the current composition rate. If the frame is presented late to the DWM or the DWM is late in composing, a frame could be displayed for fewer than the number of refreshes requested or even skipped completely.



