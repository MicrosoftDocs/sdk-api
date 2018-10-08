---
UID: NF:winuser.CreateSyntheticPointerDevice
title: CreateSyntheticPointerDevice function
author: windows-sdk-content
description: Configures the pointer injection device for the calling application, and initializes the maximum number of simultaneous pointers that the app can inject.
old-location: input_pointerdevice\createsyntheticpointerdevice.htm
tech.root: Input_PointerDevice
ms.assetid: 251F837F-DF9A-4A94-B790-73AA7196E4A9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CreateSyntheticPointerDevice, CreateSyntheticPointerDevice function, input_pointerdevice.createsyntheticpointerdevice, winuser/CreateSyntheticPointerDevice
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - CreateSyntheticPointerDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateSyntheticPointerDevice function


## -description


Configures the pointer injection device for the calling application, and initializes the maximum number of simultaneous pointers that the app can inject.


## -parameters




### -param pointerType [in]

The pointer injection device type. Must be either <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a> or <b>PT_PEN</b>.


### -param maxCount [in]

The maximum number of contacts. 


For <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a> this value must be greater than 0 and less than or equal to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_touchinjection/constants">MAX_TOUCH_COUNT</a>. 

For <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a> this value must be 1.


### -param mode [in]

The contact visualization mode.

For <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a> this must be one of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_DEFAULT</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_INDIRECT</a>, or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_NONE</a>. For more information about touch feedback settings, see <a href="https://docs.microsoft.com/windows/desktop/api/_input_touchinjection/">InitializeTouchInjection</a>. 


For <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_PEN</a> this must be one of <a href="input_pointerdevice.pointer_feedback_mode">PEN_FEEDBACK_DEFAULT</a>, <b>PEN_FEEDBACK_INDIRECT</b>, or <b>PEN_FEEDBACK_NONE</b>.


## -returns



If the function succeeds, the return value is a handle to the pointer injection device.



