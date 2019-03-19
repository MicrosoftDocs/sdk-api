---
UID: NF:winuser.GetDisplayAutoRotationPreferencesByProcessId
title: GetDisplayAutoRotationPreferencesByProcessId function (winuser.h)
author: windows-sdk-content
description: Retrieves the screen auto-rotation preferences for the process indicated by the dwProcessId parameter.
old-location: base\getdisplayautorotationpreferencesbyprocessid.htm
tech.root: ProcThread
ms.assetid: 34A769D0-5160-4049-9C72-76BA7F8B8260
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDisplayAutoRotationPreferencesByProcessId, GetDisplayAutoRotationPreferencesByProcessId function, base.getdisplayautorotationpreferencesbyprocessid, winuser/GetDisplayAutoRotationPreferencesByProcessId
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
api_name:
 - GetDisplayAutoRotationPreferencesByProcessId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Applications should use <a href="https://msdn.microsoft.com/48D609CC-3E2B-4E0E-9566-FE02853DD831">GetDisplayAutoRotationPreferences</a> to retrieve their auto-rotation preferences instead of using this API. For an example, see <a href="https://msdn.microsoft.com/48D609CC-3E2B-4E0E-9566-FE02853DD831">GetDisplayAutoRotationPreferences</a>.



