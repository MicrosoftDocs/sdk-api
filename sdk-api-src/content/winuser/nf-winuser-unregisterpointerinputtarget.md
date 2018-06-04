---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# UnregisterPointerInputTarget function


## -description


Allows the caller to unregister a target window to which all pointer input of the specified type is redirected.


## -parameters




### -param hwnd [in]

Window to be un-registered as a global redirection target on its desktop.


### -param pointerType [in]

Type of pointer input to no longer be redirected to the specified window. This is any valid and supported value from the <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">POINTER_INPUT_TYPE </a> enumeration. Note that the generic <b>PT_POINTER</b> type and the<b> PT_MOUSE</b> type are not valid in this parameter.


## -returns



If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



An application that has successfully called the <a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-09fe530f1830">RegisterPointerInputTarget</a> function can call this function to un-register the window from the role of global redirected target for the specified pointer type.

An application that has registered the same window as a global redirection target for multiple pointer input types can call the <b>UnregisterPointerInputTarget</b> to un-register the window for one of those types while leaving the window registered for the remaining types.

If the calling thread does not have the UI Access privilege, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

If the specified pointer input type is not valid, this function fails with the last error set to <b>ERROR_INVALID_PARAMETER</b>.

If the calling thread does not own the specified window, this function fails with the last error set to <b>ERROR_ACCESS_DENIED</b>.

If the specified window is not the registered global redirection target for the specified pointer input type on its desktop, this function takes no action and returns success.



