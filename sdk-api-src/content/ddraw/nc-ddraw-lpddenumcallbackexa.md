---
UID: NC:ddraw.LPDDENUMCALLBACKEXA
title: LPDDENUMCALLBACKEXA (ddraw.h)
description: The DDEnumCallbackEx function is an application-defined callback function for the DirectDrawEnumerateEx function. (ANSI)
helpviewer_keywords: ["DDEnumCallbackEx","DDEnumCallbackEx callback function [DirectDraw]","LPDDENUMCALLBACKEX","LPDDENUMCALLBACKEX callback","LPDDENUMCALLBACKEXA","LPDDENUMCALLBACKEXW","ddraw/DDEnumCallbackEx","directdraw.ddenumcallbackex"]
old-location: directdraw\ddenumcallbackex.htm
tech.root: directdraw
ms.assetid: D3D31978-D450-40B3-8C61-1F2662C1BA50
ms.date: 12/05/2018
ms.keywords: DDEnumCallbackEx, DDEnumCallbackEx callback function [DirectDraw], LPDDENUMCALLBACKEX, LPDDENUMCALLBACKEX callback, LPDDENUMCALLBACKEXA, LPDDENUMCALLBACKEXW, ddraw/DDEnumCallbackEx, directdraw.ddenumcallbackex
f1_keywords:
- ddraw/DDEnumCallbackEx
dev_langs:
- c++
req.header: ddraw.h
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ddraw.h
api_name:
- DDEnumCallbackEx
- lpddenumcallbackexa
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

The <i>DDEnumCallbackEx</i> function is an application-defined callback function for the <a href="/windows/desktop/api/ddraw/nf-ddraw-directdrawenumerateexa">DirectDrawEnumerateEx</a> function.

## -parameters

### -param unnamedParam1

A pointer to the unique identifier of the DirectDraw object.

### -param unnamedParam2

Address of a string that contains the driver name.

### -param unnamedParam3

Address of a string that contains the driver description.

### -param unnamedParam4

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.

### -param unnamedParam5

Handle of the monitor that is associated with the enumerated DirectDraw object. This parameter is NULL when the enumerated DirectDraw object is for the primary device, a nondisplay device (such as a 3-D accelerator with no 2-D capabilities), or devices not attached to the desktop.

## -returns

The callback function returns nonzero to continue the enumeration.

It returns zero to stop the enumeration.

## -remarks

After the <a href="/windows/desktop/api/ddraw/nf-ddraw-directdrawenumerateexa">DirectDrawEnumerateEx</a> function completes, the pointer to the GUID at <i>lpGUID</i> is no longer valid. You must save a copy of the GUID structure itself, not the pointer, or the <a href="/windows/desktop/api/ddraw/nf-ddraw-directdrawcreateex">DirectDrawCreateEx</a> function fails.

You can use the LPDDENUMCALLBACKEX data type to declare a variable that can contain a pointer to this callback function.

If UNICODE is defined, the string values are returned as type LPWSTR, rather than LPSTR.

> [!NOTE]
> The ddraw.h header defines LPDDENUMCALLBACKEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
