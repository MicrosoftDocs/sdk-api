---
UID: NF:winuser.GetDisplayAutoRotationPreferences
title: GetDisplayAutoRotationPreferences function (winuser.h)
author: windows-sdk-content
description: Retrieves the screen auto-rotation preferences for the current process.
old-location: base\getdisplayautorotationpreferences.htm
tech.root: ProcThread
ms.assetid: 48D609CC-3E2B-4E0E-9566-FE02853DD831
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDisplayAutoRotationPreferences, GetDisplayAutoRotationPreferences function, base.getdisplayautorotationpreferences, winuser/GetDisplayAutoRotationPreferences
ms.topic: function
f1_keywords: 
 - "winuser/GetDisplayAutoRotationPreferences"
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
 - GetDisplayAutoRotationPreferences
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetDisplayAutoRotationPreferences function


## -description


Retrieves the screen auto-rotation preferences for the current process.


## -parameters




### -param pOrientation [out]

Pointer to a location in memory that will receive the current orientation preference setting for the calling process.


## -returns



TRUE if the method succeeds, otherwise FALSE.



