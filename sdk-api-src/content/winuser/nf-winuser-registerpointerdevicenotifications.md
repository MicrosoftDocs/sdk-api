---
UID: NF:winuser.RegisterPointerDeviceNotifications
title: RegisterPointerDeviceNotifications function
author: windows-sdk-content
description: Registers a window to process the WM_POINTERDEVICECHANGE, WM_POINTERDEVICEINRANGE, and WM_POINTERDEVICEOUTOFRANGE pointer device notifications.
old-location: input_pointerdevice\registerpointerdevicenotifications.htm
tech.root: Input_PointerDevice
ms.assetid: a7322d97-f96c-449d-94a6-2081962ec7ed
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: RegisterPointerDeviceNotifications, RegisterPointerDeviceNotifications function, input_pointerdevice.registerpointerdevicenotifications, unifiedinputstack.registerpointerdevicenotifications, winuser/RegisterPointerDeviceNotifications
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RegisterPointerDeviceNotifications
: 
---

# RegisterPointerDeviceNotifications function


## -description


Registers a window to process the <a href="https://msdn.microsoft.com/9ED01D4C-58B4-4A21-B510-784281F9A909">WM_POINTERDEVICECHANGE</a>,
<a href="https://msdn.microsoft.com/04244758-E662-4FB2-850E-20B4B3D1294A">WM_POINTERDEVICEINRANGE</a>, and
<a href="https://msdn.microsoft.com/6BC667C1-6D9A-4E69-BAC6-761A1859F09E">WM_POINTERDEVICEOUTOFRANGE</a> pointer device notifications.


## -parameters




### -param window [in]

The window that receives <a href="https://msdn.microsoft.com/9ED01D4C-58B4-4A21-B510-784281F9A909">WM_POINTERDEVICECHANGE</a>,
<a href="https://msdn.microsoft.com/04244758-E662-4FB2-850E-20B4B3D1294A">WM_POINTERDEVICEINRANGE</a>, and
<a href="https://msdn.microsoft.com/6BC667C1-6D9A-4E69-BAC6-761A1859F09E">WM_POINTERDEVICEOUTOFRANGE</a> notifications.


### -param notifyRange [in]

If set to TRUE, process the <a href="https://msdn.microsoft.com/04244758-E662-4FB2-850E-20B4B3D1294A">WM_POINTERDEVICEINRANGE</a> and
<a href="https://msdn.microsoft.com/6BC667C1-6D9A-4E69-BAC6-761A1859F09E">WM_POINTERDEVICEOUTOFRANGE</a> messages. If set to FALSE, these messages aren't processed.


## -returns



If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.





## -see-also




<a href="https://msdn.microsoft.com/44942954-3EA6-4C33-8CF1-E8BF72A914CB">Functions</a>
 

 

