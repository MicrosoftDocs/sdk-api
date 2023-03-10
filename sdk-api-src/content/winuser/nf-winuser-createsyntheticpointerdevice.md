---
UID: NF:winuser.CreateSyntheticPointerDevice
title: CreateSyntheticPointerDevice function (winuser.h)
description: Configures the pointer injection device for the calling application, and initializes the maximum number of simultaneous pointers that the app can inject.
helpviewer_keywords: ["CreateSyntheticPointerDevice","CreateSyntheticPointerDevice function","input_pointerdevice.createsyntheticpointerdevice","winuser/CreateSyntheticPointerDevice"]
old-location: input_pointerdevice\createsyntheticpointerdevice.htm
tech.root: controls
ms.assetid: 251F837F-DF9A-4A94-B790-73AA7196E4A9
ms.date: 12/05/2018
ms.keywords: CreateSyntheticPointerDevice, CreateSyntheticPointerDevice function, input_pointerdevice.createsyntheticpointerdevice, winuser/CreateSyntheticPointerDevice
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - CreateSyntheticPointerDevice
 - winuser/CreateSyntheticPointerDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - CreateSyntheticPointerDevice
---

# CreateSyntheticPointerDevice function


## -description

Configures the pointer injection device for the calling application, and initializes the maximum number of simultaneous pointers that the app can inject.

## -parameters

### -param pointerType [in]

The pointer injection device type. Must be either <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a> or <b>PT_PEN</b>.

### -param maxCount [in]

The maximum number of contacts. 


For <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a> this value must be greater than 0 and less than or equal to <a href="/previous-versions/windows/desktop/input_touchinjection/constants">MAX_TOUCH_COUNT</a>. 

For <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_PEN</a> this value must be 1.

### -param mode [in]

The contact visualization mode.

## -returns

If the function succeeds, the return value is a handle to the pointer injection device. Otherwise, it returns null. To retrieve extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.