---
UID: NF:winuser.SetThreadCursorCreationScaling
title: SetThreadCursorCreationScaling function (winuser.h)
description: Sets the DPI scale for which the cursors being created on this thread are intended. This value is taken into account when scaling the cursor for the specific monitor on which it is being shown.
helpviewer_keywords: SetThreadCursorCreationScaling
ms.date: 09/23/2021
tech.root: hidpi
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winuser.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: User32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - SetThreadCursorCreationScaling
f1_keywords:
 - SetThreadCursorCreationScaling
 - winuser/SetThreadCursorCreationScaling
dev_langs:
 - c++
---

## -description

Sets the DPI scale for which the cursors being created on this thread are intended. This value is taken into account when scaling the cursor for the specific monitor on which it is being shown.

## -parameters

### -param cursorDpi

The 96-based DPI scale of the cursors that the application will be creating. For example, a 96 DPI value corresponds to 100% monitor scale factor, 144 DPI corresponds to 150%, and so on.

There are two special values:

CURSOR_CREATION_SCALING_DEFAULT – resets cursor scaling to default system behavior (as if SetThreadCursorCreationScaling was never called on this thread).

CURSOR_CREATION_SCALING_NONE – disables all cursor scaling (the cursors created after calling SetThreadCursorCreationScaling with this parameter will never be scaled up or down on any monitor).

## -returns

The previous value set for the thread before calling this API.

## -remarks

## -see-also
