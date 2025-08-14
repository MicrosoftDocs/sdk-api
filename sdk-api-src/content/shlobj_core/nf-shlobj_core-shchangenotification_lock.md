---
UID: NF:shlobj_core.SHChangeNotification_Lock
title: SHChangeNotification_Lock function (shlobj_core.h)
description: Locks the shared memory associated with a Shell change notification event.
helpviewer_keywords: ["SHChangeNotification_Lock","SHChangeNotification_Lock function [Windows Shell]","_win32_SHChangeNotification_Lock","shell.SHChangeNotification_Lock","shlobj_core/SHChangeNotification_Lock"]
old-location: shell\SHChangeNotification_Lock.htm
tech.root: shell
ms.assetid: 8e22d5d0-64be-403c-982d-c23705d85223
ms.date: 12/05/2018
ms.keywords: SHChangeNotification_Lock, SHChangeNotification_Lock function [Windows Shell], _win32_SHChangeNotification_Lock, shell.SHChangeNotification_Lock, shlobj_core/SHChangeNotification_Lock
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHChangeNotification_Lock
 - shlobj_core/SHChangeNotification_Lock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-changenotify-l1-1-1.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHChangeNotification_Lock
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHChangeNotification_Lock function


## -description

Locks the shared memory associated with a Shell change notification event.

## -parameters

### -param hChange [in]

Type: <b>HANDLE</b>

A handle to a window received as a <i>wParam</i> in the specified Shell change notification message.

### -param dwProcId

Type: <b>DWORD</b>

The process ID (<i>lParam</i> in the message callback).

### -param pppidl [out, optional]

Type: <b>PIDLIST_ABSOLUTE**</b>

The address of a pointer to a PIDLIST_ABSOLUTE that, when this function returns successfully, receives the list of affected PIDLs.

### -param plEvent [out, optional]

Type: <b>LONG*</b>

A pointer to a LONG value that, when this function returns successfully, receives the Shell change notification ID of the event that took place.

## -returns

Type: <b>HANDLE</b>

Returns a handle (HLOCK) to the locked memory. Pass this value to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock">SHChangeNotification_Unlock</a> when finished.
