---
UID: NF:winuser.IsValidDpiAwarenessContext
title: IsValidDpiAwarenessContext function (winuser.h)
description: Determines if a specified DPI_AWARENESS_CONTEXT is valid and supported by the current system.
helpviewer_keywords: ["IsValidDpiAwarenessContext","IsValidDpiAwarenessContext function [High DPI]","hidpi.isvaliddpiawarenesscontext","winuser/IsValidDpiAwarenessContext"]
old-location: hidpi\isvaliddpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: 66F48B95-DEF4-4422-BF4F-5EBA3C713A80
ms.date: 12/05/2018
ms.keywords: IsValidDpiAwarenessContext, IsValidDpiAwarenessContext function [High DPI], hidpi.isvaliddpiawarenesscontext, winuser/IsValidDpiAwarenessContext
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
 - IsValidDpiAwarenessContext
 - winuser/IsValidDpiAwarenessContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsValidDpiAwarenessContext
---

# IsValidDpiAwarenessContext function


## -description

Determines if a specified <b>DPI_AWARENESS_CONTEXT</b> is valid and supported by the current system.

## -parameters

### -param value [in]

The context that you want to determine if it is supported.

## -returns

<b>TRUE</b> if the provided context is supported, otherwise <b>FALSE</b>.

## -remarks

<b>IsValidDpiAwarenessContext</b> determines the validity of any provided <b>DPI_AWARENESS_CONTEXT</b>. You should make sure a context is valid before using <a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a> to that context.

An input <i>value</i> of <b>NULL</b> is considered to be an invalid context and will result in a return value of <b>FALSE.</b>