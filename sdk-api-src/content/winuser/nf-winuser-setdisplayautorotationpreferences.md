---
UID: NF:winuser.SetDisplayAutoRotationPreferences
title: SetDisplayAutoRotationPreferences function (winuser.h)
description: Sets the screen auto-rotation preferences for the current process.
helpviewer_keywords: ["SetDisplayAutoRotationPreferences","SetDisplayAutoRotationPreferences function","base.setdisplayautorotationpreferences","winuser/SetDisplayAutoRotationPreferences"]
old-location: base\setdisplayautorotationpreferences.htm
tech.root: backup
ms.assetid: 99A92E92-7FED-468C-9A00-D8D4B212CBFF
ms.date: 12/05/2018
ms.keywords: SetDisplayAutoRotationPreferences, SetDisplayAutoRotationPreferences function, base.setdisplayautorotationpreferences, winuser/SetDisplayAutoRotationPreferences
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetDisplayAutoRotationPreferences
 - winuser/SetDisplayAutoRotationPreferences
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
 - SetDisplayAutoRotationPreferences
---

# SetDisplayAutoRotationPreferences function


## -description

Sets the screen auto-rotation preferences for the current process.

## -parameters

### -param orientation [in]

Pointer to a location in memory with the screen orientation preferences to set for the calling process.

## -returns

TRUE if the method succeeds, otherwise FALSE.

See <a href="/windows/desktop/api/winuser/nf-winuser-getdisplayautorotationpreferences">GetDisplayAutoRotationPreferences</a> for an example of using this function.