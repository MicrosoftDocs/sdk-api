---
UID: NF:winuser.UnregisterDeviceNotification
title: UnregisterDeviceNotification function (winuser.h)
description: Closes the specified device notification handle.helpviewer_keywords: ["UnregisterDeviceNotification","UnregisterDeviceNotification function","_win32_unregisterdevicenotification","base.unregisterdevicenotification","winuser/UnregisterDeviceNotification"]
old-location: base\unregisterdevicenotification.htm
tech.root: devio
ms.assetid: bcc0cf87-f996-47b5-937c-14a6332d00d9
ms.date: 12/05/2018
ms.keywords: UnregisterDeviceNotification, UnregisterDeviceNotification function, _win32_unregisterdevicenotification, base.unregisterdevicenotification, winuser/UnregisterDeviceNotification
f1_keywords:
- winuser/UnregisterDeviceNotification
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
- Ext-MS-Win-NTUser-Misc-l1-1-0.dll
- Ext-MS-Win-NTUser-Misc-l1-2-0.dll
- Ext-MS-Win-NTUser-Misc-l1-3-0.dll
- ext-ms-win-ntuser-misc-l1-3-1.dll
- Ext-MS-Win-NTUser-Misc-L1-4-0.dll
- Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
- Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
- UnregisterDeviceNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UnregisterDeviceNotification function


## -description


Closes the specified device notification handle.


## -parameters




### -param Handle [in]

Device notification handle returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-functions">Device Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-notifications">Device Notifications</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>
 

 

