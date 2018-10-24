---
UID: NF:winuser.GetAutoRotationState
title: GetAutoRotationState function
author: windows-sdk-content
description: Retrieves an AR_STATE value containing the state of screen auto-rotation for the system, for example whether auto-rotation is supported, and whether it is enabled by the user.
old-location: base\getautorotationstate.htm
tech.root: ProcThread
ms.assetid: E041717B-920E-44F8-AC7F-B30CB82F1476
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetAutoRotationState, GetAutoRotationState function, base.getautorotationstate, winuser/GetAutoRotationState
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
 - GetAutoRotationState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAutoRotationState function


## -description


Retrieves an <a href="https://msdn.microsoft.com/55BCB2EB-524D-478A-8DCE-53E59DD0822D">AR_STATE</a> value containing the state of screen auto-rotation for the system, for example whether auto-rotation is supported, and whether it is enabled by the user. <b>GetAutoRotationState</b> provides a robust and diverse way of querying for auto-rotation state, and more. For example, if you want your app to behave differently when multiple monitors are attached then you can determine that from the <b>AR_STATE</b> returned.


## -parameters




### -param pState [out]

Pointer to a location in memory that will receive the current state of auto-rotation for the system.


## -returns



TRUE if the method succeeds, otherwise FALSE.

See <a href="https://msdn.microsoft.com/48D609CC-3E2B-4E0E-9566-FE02853DD831">GetDisplayAutoRotationPreferences</a> for an example of using this function.



