---
UID: NF:winuser.UnregisterDeviceNotification
title: UnregisterDeviceNotification function
author: windows-driver-content
description: Closes the specified device notification handle.
old-location: base\unregisterdevicenotification.htm
old-project: DevIO
ms.assetid: bcc0cf87-f996-47b5-937c-14a6332d00d9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: UnregisterDeviceNotification, UnregisterDeviceNotification function, _win32_unregisterdevicenotification, base.unregisterdevicenotification, winuser/UnregisterDeviceNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-Misc-l1-1-0.dll
-	Ext-MS-Win-NTUser-Misc-l1-2-0.dll
-	Ext-MS-Win-NTUser-Misc-l1-3-0.dll
-	ext-ms-win-ntuser-misc-l1-3-1.dll
-	Ext-MS-Win-NTUser-Misc-L1-4-0.dll
-	Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
-	Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
-	UnregisterDeviceNotification
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UnregisterDeviceNotification function


## -description


Closes the specified device notification handle.


## -parameters




### -param Handle [in]

Device notification handle returned by the 
<a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/3918ba49-1549-4f0c-b9fd-303ef46b810e">Device Management Functions</a>



<a href="https://msdn.microsoft.com/672ad753-210b-41c3-b8c7-e041ce7b1671">Device Notifications</a>



<a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a>



<a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a>
 

 

