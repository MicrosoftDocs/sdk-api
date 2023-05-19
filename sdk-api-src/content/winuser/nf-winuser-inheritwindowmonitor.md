---
UID: NF:winuser.InheritWindowMonitor
tech.root: hidpi
title: InheritWindowMonitor
ms.date: 04/21/2023
targetos: Windows
description: Causes a specified window to inherit the monitor of another window.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: User32.dll
req.header: winuser.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: User32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - InheritWindowMonitor
f1_keywords:
 - InheritWindowMonitor
 - winuser/InheritWindowMonitor
dev_langs:
 - c++
helpviewer_keywords:
 - InheritWindowMonitor
---

## -description

Causes a specified window to inherit the monitor of another window.

## -parameters

### -param hwnd

An HWND handle to the window for which monitor inheritance is set. 

### -param hwndInherit

An HWND handle to the window from which the monitor is inherited. 

## -returns

True if the call is successful.

## -remarks

## -see-also

