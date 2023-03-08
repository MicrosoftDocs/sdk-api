---
UID: NF:winuser.RegisterPointerDeviceNotifications
title: RegisterPointerDeviceNotifications function (winuser.h)
description: Registers a window to process the WM_POINTERDEVICECHANGE, WM_POINTERDEVICEINRANGE, and WM_POINTERDEVICEOUTOFRANGE pointer device notifications.
helpviewer_keywords: ["RegisterPointerDeviceNotifications","RegisterPointerDeviceNotifications function","input_pointerdevice.registerpointerdevicenotifications","unifiedinputstack.registerpointerdevicenotifications","winuser/RegisterPointerDeviceNotifications"]
old-location: input_pointerdevice\registerpointerdevicenotifications.htm
tech.root: controls
ms.assetid: a7322d97-f96c-449d-94a6-2081962ec7ed
ms.date: 12/05/2018
ms.keywords: RegisterPointerDeviceNotifications, RegisterPointerDeviceNotifications function, input_pointerdevice.registerpointerdevicenotifications, unifiedinputstack.registerpointerdevicenotifications, winuser/RegisterPointerDeviceNotifications
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - RegisterPointerDeviceNotifications
 - winuser/RegisterPointerDeviceNotifications
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-RTCore-NTUser-WMPointer-L1-1-0.dll
api_name:
 - RegisterPointerDeviceNotifications
req.apiset: ext-ms-win-rtcore-ntuser-wmpointer-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# RegisterPointerDeviceNotifications function


## -description

Registers a window to process the <a href="/windows/win32/inputmsg/wm-pointerdevicechange">WM_POINTERDEVICECHANGE</a>,
<a href="/windows/win32/inputmsg/wm-pointerdeviceinrange">WM_POINTERDEVICEINRANGE</a>, and
<a href="/windows/win32/inputmsg/wm-pointerdeviceoutofrange">WM_POINTERDEVICEOUTOFRANGE</a> pointer device notifications.

## -parameters

### -param window [in]

The window that receives <a href="/windows/win32/inputmsg/wm-pointerdevicechange">WM_POINTERDEVICECHANGE</a>,
<a href="/windows/win32/inputmsg/wm-pointerdeviceinrange">WM_POINTERDEVICEINRANGE</a>, and
<a href="/windows/win32/inputmsg/wm-pointerdeviceoutofrange">WM_POINTERDEVICEOUTOFRANGE</a> notifications.

### -param notifyRange [in]

If set to TRUE, process the <a href="/windows/win32/inputmsg/wm-pointerdeviceinrange">WM_POINTERDEVICEINRANGE</a> and
<a href="/windows/win32/inputmsg/wm-pointerdeviceoutofrange">WM_POINTERDEVICEOUTOFRANGE</a> messages. If set to FALSE, these messages aren't processed.

## -returns

If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/input_pointerdevice/functions">Functions</a>
