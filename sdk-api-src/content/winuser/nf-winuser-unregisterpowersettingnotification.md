---
UID: NF:winuser.UnregisterPowerSettingNotification
title: UnregisterPowerSettingNotification function (winuser.h)
description: Unregisters the power setting notification.
helpviewer_keywords: ["UnregisterPowerSettingNotification","UnregisterPowerSettingNotification function","base.unregisterpowersettingnotification","winuser/UnregisterPowerSettingNotification"]
old-location: base\unregisterpowersettingnotification.htm
tech.root: base
ms.assetid: de1509f5-cf4c-448e-bb3b-08da6be53bfa
ms.date: 12/05/2018
ms.keywords: UnregisterPowerSettingNotification, UnregisterPowerSettingNotification function, base.unregisterpowersettingnotification, winuser/UnregisterPowerSettingNotification
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnregisterPowerSettingNotification
 - winuser/UnregisterPowerSettingNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-powermanagement-l1-1-0.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-powermanagement-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-powermanagement-l1-1-0.dll
api_name:
 - UnregisterPowerSettingNotification
req.apiset: ext-ms-win-ntuser-powermanagement-l1-1-0 (introduced in Windows 8)
---

# UnregisterPowerSettingNotification function


## -description

Unregisters the power setting notification.

## -parameters

### -param Handle [in]

The handle returned from the <a href="/windows/desktop/api/winuser/nf-winuser-registerpowersettingnotification">RegisterPowerSettingNotification</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerpowersettingnotification">RegisterPowerSettingNotification</a>
