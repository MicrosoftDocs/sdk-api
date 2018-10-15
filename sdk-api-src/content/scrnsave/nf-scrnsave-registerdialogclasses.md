---
UID: NF:scrnsave.RegisterDialogClasses
title: RegisterDialogClasses function
author: windows-sdk-content
description: Registers any nonstandard window classes required by a screen saver's configuration dialog box.
old-location: shell\RegisterDialogClasses.htm
tech.root: shell
ms.assetid: abd3ba28-a5a7-4ace-99b1-c42f5d81930e
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: RegisterDialogClasses, RegisterDialogClasses function [Windows Shell], _win32_RegisterDialogClasses, scrnsave/RegisterDialogClasses, shell.RegisterDialogClasses
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: scrnsave.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Scrnsave.lib
req.dll: None
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - RegisterDialogClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

