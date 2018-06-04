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

# RegisterDialogClasses function


## -description


Registers any nonstandard window classes required by a screen saver's configuration dialog box.


## -parameters




### -param hInst

Type: <b>HANDLE</b>

An identifier of an instance of the module registering the window classes.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.

To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>RegisterDialogClasses</b> function should not be exported. It is called by routines defined in the Scrnsave.lib file.

If a screen saver does not register any special window classes for the configuration dialog box, the <b>RegisterDialogClasses</b> function must return <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/84c2966f-8f01-4f8d-9cec-c7fef657bff0">ScreenSaverConfigureDialog</a>
 

 

