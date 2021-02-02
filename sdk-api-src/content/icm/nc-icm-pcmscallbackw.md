---
UID: NC:icm.PCMSCALLBACKW
title: PCMSCALLBACKW
description: \**PCMSCALLBACKW** (or **ApplyCallbackFunction**) is a callback function that you implement that updates the WCS configuration data while the dialog box displayed by the [**SetupColorMatching**](setupcolormatching.md) function is executing.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - icm.h
api_name:
 - PCMSCALLBACKW
f1_keywords:
 - PCMSCALLBACKW
 - icm/PCMSCALLBACKW
dev_langs:
 - c++
---

## -description

\**PCMSCALLBACKW** (or **ApplyCallbackFunction**) is a callback function that you implement that updates the WCS configuration data while the dialog box displayed by the [**SetupColorMatching**](setupcolormatching.md) function is executing. The name **ApplyCallbackFunction** is a placeholder. The actual name of this callback function is supplied by your application using ICM.

## -parameters

### -param Arg1

Pointer to a [**COLORMATCHSETUP**](colormatchsetup.md) structure that contains WCS configuration data.

### -param Arg2

Contains a value supplied by the application.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. The callback function can set the extended error information by calling [**SetLastError**](https://www.bing.com/search?q=**SetLastError**).

## -remarks

The **ApplyCallbackFunction** function is used to change the WCS configuration for a device while the Color Management dialog box is displayed. The Color Management dialog box is displayed by the [**SetupColorMatching**](setupcolormatching.md) function.

If the callback function is provided, an **Apply** button is displayed in the lower right of the dialog box. When you select the **Apply** button, the callback function immediately updates the configuration for the device being set up. The Color Management dialog box remains on the screen.

An application supplies a callback function to WCS by storing the address of the callback function in the [**COLORMATCHSETUP**](colormatchsetup.md) structure that is passed to the [**SetupColorMatching**](setupcolormatching.md) function. The address is stored in the [**lPfnApplyCallback**](https://www.bing.com/search?q=**lPfnApplyCallback**) member of the **COLORMATCHSETUP** structure. The **dwFlags** member should be set to CMS\_USEAPPLYCALLBACK, or the callback function will be ignored.

A value supplied by the application may be passed to the callback function. Prior to invoking the [**SetupColorMatching**](setupcolormatching.md) function, the application can store a value in the [**lParamApplyCallback**](https://www.bing.com/search?q=**lParamApplyCallback**) member of the [**COLORMATCHSETUP**](colormatchsetup.md) structure. When the callback function is invoked, the value in the **lParamApplyCallback** structure member will be passed to the callback function in its *lParam* parameter.

The callback function is completely optional. If it is not supplied, the **Apply** button does not appear in the Color Management dialog box. Microsoft strongly recommends that your application supplies a callback function.

## -see-also

* [Basic color management concepts](basic-color-management-concepts.md)
* [Functions](functions.md)
* [SetupColorMatching](setupcolormatching.md)
* [COLORMATCHSETUP](colormatchsetup.md)
