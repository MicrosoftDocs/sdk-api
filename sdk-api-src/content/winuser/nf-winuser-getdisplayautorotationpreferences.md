---
UID: NF:winuser.GetDisplayAutoRotationPreferences
title: GetDisplayAutoRotationPreferences function (winuser.h)
description: Retrieves the screen auto-rotation preferences for the current process.
helpviewer_keywords: ["GetDisplayAutoRotationPreferences","GetDisplayAutoRotationPreferences function","base.getdisplayautorotationpreferences","winuser/GetDisplayAutoRotationPreferences"]
old-location: base\getdisplayautorotationpreferences.htm
tech.root: backup
ms.assetid: 48D609CC-3E2B-4E0E-9566-FE02853DD831
ms.date: 12/05/2018
ms.keywords: GetDisplayAutoRotationPreferences, GetDisplayAutoRotationPreferences function, base.getdisplayautorotationpreferences, winuser/GetDisplayAutoRotationPreferences
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCore.Lib
req.dll: Kernel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDisplayAutoRotationPreferences
 - winuser/GetDisplayAutoRotationPreferences
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-rotationmanager-l1-1-2.dll
 - kernel.dll
 - Ext-MS-Win-NTUser-rotationmanager-l1-1-1.dll
 - user32.dll
 - ext-ms-win-ntuser-rotationmanager-l1-1-0.dll
api_name:
 - GetDisplayAutoRotationPreferences
---

# GetDisplayAutoRotationPreferences function


## -description

Retrieves the screen auto-rotation preferences for the current process.

## -parameters

### -param pOrientation [out]

Pointer to a location in memory that will receive the current orientation preference setting for the calling process.

## -returns

TRUE if the method succeeds, otherwise FALSE.

