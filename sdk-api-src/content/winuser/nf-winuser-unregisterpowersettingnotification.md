---
UID: NF:winuser.UnregisterPowerSettingNotification
title: UnregisterPowerSettingNotification function
author: windows-sdk-content
description: Unregisters the power setting notification.
old-location: base\unregisterpowersettingnotification.htm
tech.root: power
ms.assetid: de1509f5-cf4c-448e-bb3b-08da6be53bfa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UnregisterPowerSettingNotification, UnregisterPowerSettingNotification function, base.unregisterpowersettingnotification, winuser/UnregisterPowerSettingNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - API-MS-Win-RTCore-NTUser-powermanagement-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-powermanagement-l1-1-0.dll
api_name:
 - UnregisterPowerSettingNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnregisterPowerSettingNotification function


## -description


Unregisters the power setting notification.


## -parameters




### -param Handle [in]

The handle returned from the <a href="https://msdn.microsoft.com/e072222e-da66-4b36-a38f-f4b618eaa391">RegisterPowerSettingNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/e072222e-da66-4b36-a38f-f4b618eaa391">RegisterPowerSettingNotification</a>
 

 

