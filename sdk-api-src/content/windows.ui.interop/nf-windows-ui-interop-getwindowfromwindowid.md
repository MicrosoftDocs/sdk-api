---
UID: NF:windows.ui.interop.GetWindowFromWindowId
tech.root: winrt
title: GetWindowFromWindowId
ms.date: 05/16/2025
targetos: Windows
description: Gets the window handle (HWND) that corresponds to the specified WindowId, if the *windowId* argument is valid and the system has an **HWND** that represents the window.
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
 - GetWindowFromWindowId
f1_keywords:
 - GetWindowFromWindowId
 - windows.ui.interop/GetWindowFromWindowId
dev_langs:
 - c++
helpviewer_keywords:
 - GetWindowFromWindowId
---

## -description

Gets the window handle ([HWND](/windows/win32/winprog/windows-data-types)) that corresponds to the specified [WindowId](/uwp/api/windows.ui.windowid), if the *windowId* argument is valid and the system has an **HWND** that represents the window.

## -parameters

### -param id

The identifier for the window.

### -param hwnd

The window handle that corresponds to *windowId*, if *windowId* is valid and the system has an **HWND** that represents the window. Otherwise, null.

## -returns

## -remarks

## -see-also

