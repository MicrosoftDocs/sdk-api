---
UID: NF:winuser.InjectSyntheticPointerInput
title: InjectSyntheticPointerInput function (winuser.h)
description: Simulates pointer input (pen or touch).
helpviewer_keywords: ["InjectSyntheticPointerInput","InjectSyntheticPointerInput function","input_pointerdevice.injectsyntheticpointerinput","winuser/InjectSyntheticPointerInput"]
old-location: input_pointerdevice\injectsyntheticpointerinput.htm
tech.root: controls
ms.assetid: 9F7FC5E2-F4B8-42C2-A4BE-240E36AFC13B
ms.date: 12/05/2018
ms.keywords: InjectSyntheticPointerInput, InjectSyntheticPointerInput function, input_pointerdevice.injectsyntheticpointerinput, winuser/InjectSyntheticPointerInput
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
 - InjectSyntheticPointerInput
 - winuser/InjectSyntheticPointerInput
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
 - InjectSyntheticPointerInput
---

# InjectSyntheticPointerInput function


## -description

Simulates pointer input (pen or touch).

## -parameters

### -param device

A handle to the pointer injection device created by <a href="../winuser/nf-winuser-createsyntheticpointerdevice.md">CreateSyntheticPointerDevice</a>.

### -param pointerInfo [in]

An array of [POINTER_TYPE_INFO](ns-winuser-pointer_type_info.md) structures represneting the injected pointers.

The type must match the <i>pointerType</i> parameter of the <a href="../winuser/nf-winuser-createsyntheticpointerdevice.md">CreateSyntheticPointerDevice</a> call that created the injection device. 


The ptPixelLocation for each POINTER_TYPE_INFO is specified relative to top left of the virtual screen:

### -param count [in]

The number of contacts. 


For <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a> this value must be greater than 0 and less than or equal to <a href="/previous-versions/windows/desktop/input_touchinjection/constants">MAX_TOUCH_COUNT</a>. 

For <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_PEN</a> this value must be 1.

## -returns

If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.
