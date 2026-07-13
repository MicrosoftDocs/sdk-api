---
UID: NF:windows.ui.interop.GetWindowIdFromWindow
tech.root: winrt
title: GetWindowIdFromWindow
ms.date: 05/16/2025
targetos: Windows
description: Gets the WindowId that corresponds to the specified window handle HWND, if the hwnd argument is valid.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windows.ui.interop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ext-ms-win-windowing-external-l1-1-0.dll
 - windows.ui.interop.h
api_name:
 - GetWindowIdFromWindow
f1_keywords:
 - GetWindowIdFromWindow
 - windows.ui.interop/GetWindowIdFromWindow
dev_langs:
 - c++
helpviewer_keywords:
 - GetWindowIdFromWindow
---

## -description

Gets the [WindowId](/uwp/api/windows.ui.windowid) that corresponds to the specified window handle ([HWND](/windows/win32/winprog/windows-data-types)), if the hwnd argument is valid.

## -parameters

### -param hwnd

The handle of the window for which to get the **WindowId**.

### -param id

The identifier that corresponds to *hwnd*, if *hwnd* is valid. Otherwise, null.

## -returns

## -remarks

## -see-also

