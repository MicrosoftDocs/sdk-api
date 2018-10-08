---
UID: NF:winuser.InjectSyntheticPointerInput
title: InjectSyntheticPointerInput function
author: windows-sdk-content
description: Simulates pointer input (pen or touch).
old-location: input_pointerdevice\injectsyntheticpointerinput.htm
tech.root: Input_PointerDevice
ms.assetid: 9F7FC5E2-F4B8-42C2-A4BE-240E36AFC13B
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: InjectSyntheticPointerInput, InjectSyntheticPointerInput function, input_pointerdevice.injectsyntheticpointerinput, winuser/InjectSyntheticPointerInput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - InjectSyntheticPointerInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InjectSyntheticPointerInput function


## -description


Simulates pointer input (pen or touch).


## -parameters




### -param device

A handle to the pointer injection device created by <a href="input_pointerdevice.createsyntheticpointerdevice">CreateSyntheticPointerDevice</a>.


### -param pointerInfo [in]

Array of injected pointers.

The type must match the <i>pointerType</i> parameter of the <a href="input_pointerdevice.createsyntheticpointerdevice">CreateSyntheticPointerDevice</a> call that created the injection device. 


For <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a> this must be one of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_DEFAULT</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_INDIRECT</a>, or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_NONE</a>. For more information about touch feedback settings, see <a href="https://docs.microsoft.com/windows/desktop/api/_input_touchinjection/">InitializeTouchInjection</a>. 


For <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a> this must be one of <a href="input_pointerdevice.pointer_feedback_mode">PEN_FEEDBACK_DEFAULT</a>, <b>PEN_FEEDBACK_INDIRECT</b>, or <b>PEN_FEEDBACK_NONE</b>.

The ptPixelLocation for each POINTER_TYPE_INFO is specified relative to top left of the virtual screen:


### -param count [in]

TBD


## -returns



If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




