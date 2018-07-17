---
UID: NF:winuser.GetDisplayAutoRotationPreferences
title: GetDisplayAutoRotationPreferences function
author: windows-sdk-content
description: Retrieves the screen auto-rotation preferences for the current process.
old-location: base\getdisplayautorotationpreferences.htm
old-project: procthread
ms.assetid: 48D609CC-3E2B-4E0E-9566-FE02853DD831
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetDisplayAutoRotationPreferences, GetDisplayAutoRotationPreferences function, base.getdisplayautorotationpreferences, winuser/GetDisplayAutoRotationPreferences
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
 - GetDisplayAutoRotationPreferences
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetDisplayAutoRotationPreferences function


## -description


Retrieves the screen auto-rotation preferences for the current process.


## -parameters




### -param pOrientation [out]

Pointer to a location in memory that will receive the current orientation preference setting for the calling process.


## -returns



TRUE if the method succeeds, otherwise FALSE.



