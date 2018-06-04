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

# GetDialogControlDpiChangeBehavior function


## -description


Retrieves and per-monitor DPI scaling behavior overrides of a child window in a dialog.


## -parameters




### -param hWnd

The handle for the window to examine.


## -returns



The flags set on the given window. If passed an invalid handle, this function will return zero, and set its <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">last error</a> to <b>ERROR_INVALID_HANDLE</b>.




## -see-also




<a href="https://msdn.microsoft.com/B368D997-F409-491A-8578-004C7408A160">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>



<a href="https://msdn.microsoft.com/52BB557B-0D70-4189-9BD0-EB94188EA4E7">SetDialogControlDpiChangeBehavior</a>
 

 

