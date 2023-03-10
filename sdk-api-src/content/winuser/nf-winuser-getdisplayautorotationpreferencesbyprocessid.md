---
UID: NF:winuser.GetDisplayAutoRotationPreferencesByProcessId
title: GetDisplayAutoRotationPreferencesByProcessId function (winuser.h)
description: Retrieves the screen auto-rotation preferences for the process indicated by the dwProcessId parameter.
helpviewer_keywords: ["GetDisplayAutoRotationPreferencesByProcessId","GetDisplayAutoRotationPreferencesByProcessId function","base.getdisplayautorotationpreferencesbyprocessid","winuser/GetDisplayAutoRotationPreferencesByProcessId"]
old-location: base\getdisplayautorotationpreferencesbyprocessid.htm
tech.root: backup
ms.assetid: 34A769D0-5160-4049-9C72-76BA7F8B8260
ms.date: 12/05/2018
ms.keywords: GetDisplayAutoRotationPreferencesByProcessId, GetDisplayAutoRotationPreferencesByProcessId function, base.getdisplayautorotationpreferencesbyprocessid, winuser/GetDisplayAutoRotationPreferencesByProcessId
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
 - GetDisplayAutoRotationPreferencesByProcessId
 - winuser/GetDisplayAutoRotationPreferencesByProcessId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel.dll
api_name:
 - GetDisplayAutoRotationPreferencesByProcessId
---

# GetDisplayAutoRotationPreferencesByProcessId function


## -description

Retrieves the screen auto-rotation preferences for the process indicated by the <i>dwProcessId</i> parameter.

## -parameters

### -param dwProcessId [in]

The process to get preference settings for.

### -param pOrientation [out]

Pointer to a location in memory that will receive the current orientation preference setting for the indicated process.

### -param fRotateScreen [out]

Pointer to a location in memory that will receive a TRUE or FALSE value indicating whether the screen was rotated to comply with the process orientation preferences.

## -returns

TRUE if the method succeeds, otherwise FALSE.

Applications should use <a href="/windows/desktop/api/winuser/nf-winuser-getdisplayautorotationpreferences">GetDisplayAutoRotationPreferences</a> to retrieve their auto-rotation preferences instead of using this API. For an example, see <a href="/windows/desktop/api/winuser/nf-winuser-getdisplayautorotationpreferences">GetDisplayAutoRotationPreferences</a>.