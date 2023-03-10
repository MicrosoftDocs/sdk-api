---
UID: NF:winuser.GetGestureExtraArgs
title: GetGestureExtraArgs function (winuser.h)
description: Retrieves additional information about a gesture from its GESTUREINFO handle.
helpviewer_keywords: ["GetGestureExtraArgs","GetGestureExtraArgs function [Windows Touch]","wintouch.getgestureextraargs","winuser/GetGestureExtraArgs"]
old-location: wintouch\getgestureextraargs.htm
tech.root: wintouch
ms.assetid: f7775d88-6a5b-4283-ab40-65c2da218f81
ms.date: 12/05/2018
ms.keywords: GetGestureExtraArgs, GetGestureExtraArgs function [Windows Touch], wintouch.getgestureextraargs, winuser/GetGestureExtraArgs
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
ms.custom: 19H1
f1_keywords:
 - GetGestureExtraArgs
 - winuser/GetGestureExtraArgs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - GetGestureExtraArgs
---

# GetGestureExtraArgs function


## -description

Retrieves additional information about a gesture from its <a href="/windows/desktop/api/winuser/ns-winuser-gestureinfo">GESTUREINFO</a> handle.

## -parameters

### -param hGestureInfo [in]

The handle to the gesture information that is passed in the <i>lParam</i> of a <a href="/windows/desktop/wintouch/wm-gesture">WM_GESTURE</a> message.

### -param cbExtraArgs [in]

A count of the bytes of data stored in the extra arguments.

### -param pExtraArgs [out]

A pointer to the extra argument information.

## -returns

If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

This function is reserved for future use and should only be used for testing. Windows 7 gestures do not use extra arguments.

## -see-also

<a href="/windows/desktop/wintouch/mtgfunctions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getgestureinfo">GetGestureInfo</a>



<a href="/windows/desktop/wintouch/guide-multi-touch-gestures">Programming Guide for Gestures</a>