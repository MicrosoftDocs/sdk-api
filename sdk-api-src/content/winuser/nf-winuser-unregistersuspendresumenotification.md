---
UID: NF:winuser.UnregisterSuspendResumeNotification
title: UnregisterSuspendResumeNotification function (winuser.h)
description: Cancels a registration to receive notification when the system is suspended or resumed. Similar to PowerUnregisterSuspendResumeNotification but operates in user mode.
helpviewer_keywords: ["UnregisterSuspendResumeNotification","UnregisterSuspendResumeNotification function","base.unregistersuspendresumenotification","winuser/UnregisterSuspendResumeNotification"]
old-location: base\unregistersuspendresumenotification.htm
tech.root: base
ms.assetid: d9307452-9670-4e9c-9df8-6a3b41d0bd2e
ms.date: 12/05/2018
ms.keywords: UnregisterSuspendResumeNotification, UnregisterSuspendResumeNotification function, base.unregistersuspendresumenotification, winuser/UnregisterSuspendResumeNotification
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
 - UnregisterSuspendResumeNotification
 - winuser/UnregisterSuspendResumeNotification
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
 - UnregisterSuspendResumeNotification
req.apiset: ext-ms-win-ntuser-powermanagement-l1-1-0 (introduced in Windows 8)
---

# UnregisterSuspendResumeNotification function


## -description

Cancels a registration to receive notification when the system is suspended or resumed. Similar to <a href="/windows/desktop/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification">PowerUnregisterSuspendResumeNotification</a> but operates in user mode.

## -parameters

### -param Handle [in, out]

A handle to a registration obtained by calling the <a href="/windows/desktop/api/winuser/nf-winuser-registersuspendresumenotification">RegisterSuspendResumeNotification</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-registersuspendresumenotification">RegisterSuspendResumeNotification</a>
