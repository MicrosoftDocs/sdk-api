---
UID: NF:powersetting.PowerSettingUnregisterNotification
title: PowerSettingUnregisterNotification function (powersetting.h)
description: Cancels a registration to receive notification when a power setting changes.
helpviewer_keywords: ["PowerSettingUnregisterNotification","PowerSettingUnregisterNotification function","base.powersettingunregisternotification","powersetting/PowerSettingUnregisterNotification","powrprof/PowerSettingUnregisterNotification"]
old-location: base\powersettingunregisternotification.htm
tech.root: base
ms.assetid: 9853c347-4528-43bb-8326-13bcd819b8a6
ms.date: 12/05/2018
ms.keywords: PowerSettingUnregisterNotification, PowerSettingUnregisterNotification function, base.powersettingunregisternotification, powersetting/PowerSettingUnregisterNotification, powrprof/PowerSettingUnregisterNotification
req.header: powersetting.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerSettingUnregisterNotification
 - powersetting/PowerSettingUnregisterNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-power-setting-l1-1-1.dll
 - Powrprof.dll
 - API-MS-Win-power-setting-l1-1-0.dll
api_name:
 - PowerSettingUnregisterNotification
---

# PowerSettingUnregisterNotification function


## -description

Cancels a registration to receive notification when a power setting changes.

## -parameters

### -param RegistrationHandle [in, out]

A handle to a registration obtained by calling the <a href="/windows/desktop/api/powersetting/nf-powersetting-powersettingregisternotification">PowerSettingRegisterNotification</a> function.

## -returns

Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed.

## -see-also

<a href="/windows/desktop/api/powersetting/nf-powersetting-powersettingregisternotification">PowerSettingRegisterNotification</a>