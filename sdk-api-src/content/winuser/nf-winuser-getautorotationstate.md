---
UID: NF:winuser.GetAutoRotationState
title: GetAutoRotationState function (winuser.h)
description: Retrieves an AR_STATE value containing the state of screen auto-rotation for the system, for example whether auto-rotation is supported, and whether it is enabled by the user.
helpviewer_keywords: ["GetAutoRotationState","GetAutoRotationState function","base.getautorotationstate","winuser/GetAutoRotationState"]
old-location: base\getautorotationstate.htm
tech.root: backup
ms.assetid: E041717B-920E-44F8-AC7F-B30CB82F1476
ms.date: 12/05/2018
ms.keywords: GetAutoRotationState, GetAutoRotationState function, base.getautorotationstate, winuser/GetAutoRotationState
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
req.lib: OneCore.Lib
req.dll: Kernel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAutoRotationState
 - winuser/GetAutoRotationState
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
 - GetAutoRotationState
---

# GetAutoRotationState function


## -description

Retrieves an <a href="/windows/desktop/api/winuser/ne-winuser-ar_state">AR_STATE</a> value containing the state of screen auto-rotation for the system, for example whether auto-rotation is supported, and whether it is enabled by the user. <b>GetAutoRotationState</b> provides a robust and diverse way of querying for auto-rotation state, and more. For example, if you want your app to behave differently when multiple monitors are attached then you can determine that from the <b>AR_STATE</b> returned.

## -parameters

### -param pState [out]

Pointer to a location in memory that will receive the current state of auto-rotation for the system.

## -returns

TRUE if the method succeeds, otherwise FALSE.

See <a href="/windows/desktop/api/winuser/nf-winuser-getdisplayautorotationpreferences">GetDisplayAutoRotationPreferences</a> for an example of using this function.