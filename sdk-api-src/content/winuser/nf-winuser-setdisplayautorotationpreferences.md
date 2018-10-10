---
UID: NF:winuser.SetDisplayAutoRotationPreferences
title: SetDisplayAutoRotationPreferences function
author: windows-sdk-content
description: Sets the screen auto-rotation preferences for the current process.
old-location: base\setdisplayautorotationpreferences.htm
tech.root: ProcThread
ms.assetid: 99A92E92-7FED-468C-9A00-D8D4B212CBFF
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: SetDisplayAutoRotationPreferences, SetDisplayAutoRotationPreferences function, base.setdisplayautorotationpreferences, winuser/SetDisplayAutoRotationPreferences
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Kernel.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel.dll
 - Ext-MS-Win-NTUser-rotationmanager-l1-1-1.dll
 - user32.dll
 - ext-ms-win-ntuser-rotationmanager-l1-1-0.dll
api_name:
 - SetDisplayAutoRotationPreferences
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetDisplayAutoRotationPreferences function


## -description


Sets the screen auto-rotation preferences for the current process.


## -parameters




### -param orientation [in]

Pointer to a location in memory with the screen orientation preferences to set for the calling process.


## -returns



TRUE if the method succeeds, otherwise FALSE.

See <a href="https://msdn.microsoft.com/48D609CC-3E2B-4E0E-9566-FE02853DD831">GetDisplayAutoRotationPreferences</a> for an example of using this function.



