---
UID: NF:shlobj_core.SHChangeNotification_Lock
title: SHChangeNotification_Lock function
author: windows-driver-content
description: Locks the shared memory associated with a Shell change notification event.
old-location: shell\SHChangeNotification_Lock.htm
old-project: shell
ms.assetid: 8e22d5d0-64be-403c-982d-c23705d85223
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: SHChangeNotification_Lock, SHChangeNotification_Lock function [Windows Shell], _win32_SHChangeNotification_Lock, shell.SHChangeNotification_Lock, shlobj_core/SHChangeNotification_Lock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	ext-ms-win-shell-shell32-l1-2-1.dll
-	Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
-	SHChangeNotification_Lock
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
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

Returns a handle (HLOCK) to the locked memory. Pass this value to <a href="https://msdn.microsoft.com/967ede1f-ee9c-46ee-a371-dcfc3a57d824">SHChangeNotification_Unlock</a> when finished.



