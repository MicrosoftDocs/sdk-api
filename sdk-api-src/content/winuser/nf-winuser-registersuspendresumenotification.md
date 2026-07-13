---
UID: NF:winuser.RegisterSuspendResumeNotification
title: RegisterSuspendResumeNotification function (winuser.h)
description: Registers to receive notification when the system is suspended or resumed. Similar to PowerRegisterSuspendResumeNotification, but operates in user mode and can take a window handle.
helpviewer_keywords: ["RegisterSuspendResumeNotification","RegisterSuspendResumeNotification function","base.registersuspendresumenotification","winuser/RegisterSuspendResumeNotification"]
old-location: base\registersuspendresumenotification.htm
tech.root: base
ms.assetid: 6cd42d32-07e9-4cbd-83f9-6146b1cb54db
ms.date: 12/05/2018
ms.keywords: RegisterSuspendResumeNotification, RegisterSuspendResumeNotification function, base.registersuspendresumenotification, winuser/RegisterSuspendResumeNotification
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
 - RegisterSuspendResumeNotification
 - winuser/RegisterSuspendResumeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - RegisterSuspendResumeNotification
req.apiset: ext-ms-win-ntuser-powermanagement-l1-1-0 (introduced in Windows 8)
---

# RegisterSuspendResumeNotification function


## -description

Registers to receive notification when the system is suspended or resumed. Similar to <a href="/windows/desktop/api/powerbase/nf-powerbase-powerregistersuspendresumenotification">PowerRegisterSuspendResumeNotification</a>, but operates in user mode and can take a window handle.

## -parameters

### -param hRecipient [in]

 This parameter contains parameters for subscribing to a power notification or a window handle representing the subscribing process. 

If <i>Flags</i> is <b>DEVICE_NOTIFY_CALLBACK</b>, <i>hRecipient</i> is interpreted as a pointer to a <a href="/windows/win32/api/powrprof/ns-powrprof-device_notify_subscribe_parameters">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a> structure. In this case, the callback function is <a href="/windows/desktop/api/powrprof/nc-powrprof-device_notify_callback_routine">DeviceNotifyCallbackRoutine</a>. When the <b>Callback</b> function executes, the  <i>Type</i> parameter is set indicating the type of event that occurred. Possible values include <b>PBT_APMSUSPEND</b>, <b>PBT_APMRESUMESUSPEND</b>, and <b>PBT_APMRESUMEAUTOMATIC</b> - see  <a href="/windows/desktop/Power/power-management-events">Power Management Events</a> for more info. The <i>Setting</i> parameter is not used with suspend/resume notifications.

If <i>Flags</i> is <b>DEVICE_NOTIFY_WINDOW_HANDLE</b>, <i>hRecipient</i> is a handle to the window to deliver events to.

### -param Flags [in]

 This parameter can be <b>DEVICE_NOTIFY_WINDOW_HANDLE</b> or <b>DEVICE_NOTIFY_CALLBACK</b>.

## -returns

A handle to the registration. Use this handle to unregister for notifications.

If the function fails, the return value is NULL. To get extended error information call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/powrprof/nc-powrprof-device_notify_callback_routine">DEVICE_NOTIFY_CALLBACK_ROUTINE</a>



<a href="/windows/win32/api/powrprof/ns-powrprof-device_notify_subscribe_parameters">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unregistersuspendresumenotification">UnregisterSuspendResumeNotification</a>
