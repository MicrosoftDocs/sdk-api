---
UID: NF:winuser.RegisterSuspendResumeNotification
title: RegisterSuspendResumeNotification function
author: windows-driver-content
description: Registers to receive notification when the system is suspended or resumed. Similar to PowerRegisterSuspendResumeNotification, but operates in user mode and can take a window handle.
old-location: base\registersuspendresumenotification.htm
old-project: Power
ms.assetid: 6cd42d32-07e9-4cbd-83f9-6146b1cb54db
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: RegisterSuspendResumeNotification, RegisterSuspendResumeNotification function, base.registersuspendresumenotification, winuser/RegisterSuspendResumeNotification
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	RegisterSuspendResumeNotification
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegisterSuspendResumeNotification function


## -description


Registers to receive notification when the system is suspended or resumed. Similar to <a href="https://msdn.microsoft.com/3b39ec3a-417c-4ce4-a581-ed967f1baec9">PowerRegisterSuspendResumeNotification</a>, but operates in user mode and can take a window handle.


## -parameters




### -param hRecipient [in]

 This parameter contains parameters for subscribing to a power notification or a window handle representing the subscribing process. 

If <i>Flags</i> is <b>DEVICE_NOTIFY_CALLBACK</b>, <i>hRecipient</i> is interpreted as a pointer to a <a href="https://msdn.microsoft.com/749F7C6F-1A42-43DE-921E-C3654034570D">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a> structure. In this case, the callback function is <a href="https://msdn.microsoft.com/5734FDEE-E330-4115-AFA5-725114023A5A">DeviceNotifyCallbackRoutine</a>. When the <b>Callback</b> function executes, the  <i>Type</i> parameter is set indicating the type of event that occurred. Possible values include <b>PBT_APMSUSPEND</b>, <b>PBT_APMRESUMESUSPEND</b>, and <b>PBT_APMRESUMEAUTOMATIC</b> - see  <a href="https://msdn.microsoft.com/2315e17f-f0c1-409c-b1c0-b3735c25c4c1">Power Management Events</a> for more info. The <i>Setting</i> parameter is not used with suspend/resume notifications.

If <i>Flags</i> is <b>DEVICE_NOTIFY_WINDOW_HANDLE</b>, <i>hRecipient</i> is a handle to the window to deliver events to. 


### -param Flags [in]

 This parameter can be <b>DEVICE_NOTIFY_WINDOW_HANDLE</b> or <b>DEVICE_NOTIFY_CALLBACK</b>.


## -returns



A handle to the registration. Use this handle to unregister for notifications.

If the function fails, the return value is NULL. To get extended error information call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/5734FDEE-E330-4115-AFA5-725114023A5A">DEVICE_NOTIFY_CALLBACK_ROUTINE</a>



<a href="https://msdn.microsoft.com/749F7C6F-1A42-43DE-921E-C3654034570D">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/d9307452-9670-4e9c-9df8-6a3b41d0bd2e">UnregisterSuspendResumeNotification</a>
 

 

