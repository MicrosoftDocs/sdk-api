---
UID: NF:userenv.RegisterGPNotification
title: RegisterGPNotification function (userenv.h)
description: The RegisterGPNotification function enables an application to receive notification when there is a change in policy. When a policy change occurs, the specified event object is set to the signaled state.
helpviewer_keywords: ["RegisterGPNotification","RegisterGPNotification function [Group Policy]","_win32_registergpnotification","policy.registergpnotification","userenv/RegisterGPNotification"]
old-location: policy\registergpnotification.htm
tech.root: Policy
ms.assetid: 0a758da3-73a8-4d9b-8663-e6cab1a1bd3f
ms.date: 12/05/2018
ms.keywords: RegisterGPNotification, RegisterGPNotification function [Group Policy], _win32_registergpnotification, policy.registergpnotification, userenv/RegisterGPNotification
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterGPNotification
 - userenv/RegisterGPNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - RegisterGPNotification
---

# RegisterGPNotification function


## -description

The
    <b>RegisterGPNotification</b> function enables an application to receive notification when there is a change in policy. When a policy change occurs, the specified event object is set to the signaled state.

## -parameters

### -param hEvent [in]

Handle to an event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create the event object.

### -param bMachine [in]

Specifies the policy change type. If <b>TRUE</b>, computer policy changes are reported. If <b>FALSE</b>, user policy changes are reported.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call the 
<a href="/windows/desktop/api/userenv/nf-userenv-unregistergpnotification">UnregisterGPNotification</a> function to unregister the handle from receiving policy change notifications. Call the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle when it is no longer required.

An application can also receive notifications about policy changes when a 
<a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a> message is broadcast. In this instance, the <i>wParam</i> parameter value is 1 if computer policy was applied; it is zero if user policy was applied. The <i>lParam</i> parameter points to the string "Policy".

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nf-userenv-unregistergpnotification">UnregisterGPNotification</a>