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

Sets the DPI scale for which the cursors being created on this thread are intended. This value is taken into account when scaling the cursor based on the current system DPI.

## -parameters

### -param cursorDpi

The 96-based DPI scale of the cursors that the application will be creating. For example, a 96 DPI value corresponds to 100% monitor scale factor, 144 DPI corresponds to 150%, and so on.

There are two special values:

`CURSOR_CREATION_SCALING_DEFAULT` – resets cursor scaling to default system behavior (as if SetThreadCursorCreationScaling was never called on this thread).

`CURSOR_CREATION_SCALING_NONE` – disables all cursor scaling. Cursors created while this value is set will always be displayed at their original pixel size, regardless of the monitor DPI. The size reported by [GetCursorInfo](nf-winuser-getcursorinfo.md) and used for hit-testing will also reflect the original size without any DPI adjustment.

## -returns

The previous value set for the thread before calling this API.

## -remarks

When loading cursors from a module resource via [LoadCursor](nf-winuser-loadcursor.md) or [LoadImage](nf-winuser-loadimagew.md), Windows automatically selects the best-matching cursor size for the current display DPI and can rescale the cursor when the window moves between monitors with different DPI values.

However, when creating cursors programmatically from in-memory data via [CreateIconFromResourceEx](nf-winuser-createiconfromresourceex.md) or [CreateCursor](nf-winuser-createcursor.md), Windows has no resource context and cannot perform automatic rescaling.

Starting with Windows 11 (Build 22000), **SetThreadCursorCreationScaling** can be used to associate a memory-created cursor with a specific DPI. Windows will then automatically generate scaled copies for all required DPI values and select the appropriate one based on the current system DPI (as returned by [GetDpiForSystem](/windows/win32/api/shellscalingapi/nf-shellscalingapi-getdpiforsystem)):

```cpp
// Create a 48x48 cursor tagged for 144 DPI (150% scale)
UINT previousDpi = SetThreadCursorCreationScaling(144);
HCURSOR hCursor = CreateCursorFrom48pxData(...);
SetThreadCursorCreationScaling(previousDpi);
```

When using **SetThreadCursorCreationScaling** together with [LoadImage](nf-winuser-loadimagew.md) on a cursor file that contains multiple sizes, the explicit `cx`/`cy` size passed to **LoadImage** must match the pixel size that corresponds to the DPI passed to **SetThreadCursorCreationScaling**. If the two values are inconsistent, the cursor size reported to the system will be incorrect, which may affect hit-testing and layout.

This mechanism works independently of the process DPI awareness mode.

**SetThreadCursorCreationScaling** only affects cursors - it has no effect on icons created via the same APIs.

## -see-also
