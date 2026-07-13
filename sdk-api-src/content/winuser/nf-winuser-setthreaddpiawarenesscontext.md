---
UID: NF:winuser.SetThreadDpiAwarenessContext
title: SetThreadDpiAwarenessContext function (winuser.h)
description: Set the DPI awareness for the current thread to the provided value.
helpviewer_keywords: ["SetThreadDpiAwarenessContext","SetThreadDpiAwarenessContext function [High DPI]","hidpi.setthreaddpiawarenesscontext","winuser/SetThreadDpiAwarenessContext"]
old-location: hidpi\setthreaddpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: 95531BDC-3D45-4BB6-8C63-0D845C66B88F
ms.date: 12/05/2018
ms.keywords: SetThreadDpiAwarenessContext, SetThreadDpiAwarenessContext function [High DPI], hidpi.setthreaddpiawarenesscontext, winuser/SetThreadDpiAwarenessContext
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - SetThreadDpiAwarenessContext
 - winuser/SetThreadDpiAwarenessContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-2.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-1.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetThreadDpiAwarenessContext
---

# SetThreadDpiAwarenessContext function


## -description

Set the DPI awareness for the current thread to the provided value.

## -parameters

### -param dpiContext [in]

The new <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for the current thread. This context includes the <a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a> value.

## -returns

The old <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for the thread. If the <i>dpiContext</i> is invalid, the thread will not be updated and the return value will be <b>NULL</b>. You can use this value to restore the old <b>DPI_AWARENESS_CONTEXT</b> after overriding it with a predefined value.

## -remarks

Use this API to change the <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for the thread from the default value for the app.

## -see-also

<a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a>