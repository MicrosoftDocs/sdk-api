---
UID: NF:winuser.UnregisterSuspendResumeNotification
title: UnregisterSuspendResumeNotification function
author: windows-sdk-content
description: Cancels a registration to receive notification when the system is suspended or resumed. Similar to PowerUnregisterSuspendResumeNotification but operates in user mode.
old-location: base\unregistersuspendresumenotification.htm
tech.root: power
ms.assetid: d9307452-9670-4e9c-9df8-6a3b41d0bd2e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UnregisterSuspendResumeNotification, UnregisterSuspendResumeNotification function, base.unregistersuspendresumenotification, winuser/UnregisterSuspendResumeNotification
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
api_name:
 - UnregisterSuspendResumeNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnregisterSuspendResumeNotification function


## -description


Cancels a registration to receive notification when the system is suspended or resumed. Similar to <a href="https://msdn.microsoft.com/5680e6bd-1694-4d5f-94ea-41b24149c741">PowerUnregisterSuspendResumeNotification</a> but operates in user mode.


## -parameters




### -param Handle [in, out]

A handle to a registration obtained by calling the <a href="https://msdn.microsoft.com/6cd42d32-07e9-4cbd-83f9-6146b1cb54db">RegisterSuspendResumeNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/6cd42d32-07e9-4cbd-83f9-6146b1cb54db">RegisterSuspendResumeNotification</a>
 

 

