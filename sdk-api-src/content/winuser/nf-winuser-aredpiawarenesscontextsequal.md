---
UID: NF:winuser.AreDpiAwarenessContextsEqual
title: AreDpiAwarenessContextsEqual function (winuser.h)
description: Determines whether two DPI_AWARENESS_CONTEXT values are identical.
helpviewer_keywords: ["AreDpiAwarenessContextsEqual","AreDpiAwarenessContextsEqual function [High DPI]","hidpi.aredpiawarenesscontextsequal","winuser/AreDpiAwarenessContextsEqual"]
old-location: hidpi\aredpiawarenesscontextsequal.htm
tech.root: hidpi
ms.assetid: 77660CAB-97ED-4DAC-A95E-A149F1A479FD
ms.date: 12/05/2018
ms.keywords: AreDpiAwarenessContextsEqual, AreDpiAwarenessContextsEqual function [High DPI], hidpi.aredpiawarenesscontextsequal, winuser/AreDpiAwarenessContextsEqual
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
 - AreDpiAwarenessContextsEqual
 - winuser/AreDpiAwarenessContextsEqual
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
 - AreDpiAwarenessContextsEqual
---

# AreDpiAwarenessContextsEqual function


## -description

Determines whether two <b>DPI_AWARENESS_CONTEXT</b> values are identical.

## -parameters

### -param dpiContextA [in]

The first value to compare.

### -param dpiContextB [in]

The second value to compare.

## -returns

Returns <b>TRUE</b> if the values are equal, otherwise <b>FALSE</b>.

## -remarks

A <b>DPI_AWARENESS_CONTEXT</b> contains multiple pieces of information. For example, it includes both the current and the inherited <a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a> values. <b>AreDpiAwarenessContextsEqual</b> ignores informational flags and determines if the values are equal. You can't use a direct bitwise comparison because of these informational flags.