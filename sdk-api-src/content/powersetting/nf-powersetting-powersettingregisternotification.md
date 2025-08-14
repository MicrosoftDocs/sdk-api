---
UID: NF:powersetting.PowerSettingRegisterNotification
title: PowerSettingRegisterNotification function (powersetting.h)
description: Registers to receive notification when a power setting changes.
helpviewer_keywords: ["DEVICE_NOTIFY_CALLBACK","DEVICE_NOTIFY_SERVICE_HANDLE","PowerSettingRegisterNotification","PowerSettingRegisterNotification function","base.powersettingregisternotification","powersetting/PowerSettingRegisterNotification","powrprof/PowerSettingRegisterNotification"]
old-location: base\powersettingregisternotification.htm
tech.root: base
ms.assetid: 0fbca717-2367-4407-8094-3eb2b717b59c
ms.date: 12/05/2018
ms.keywords: DEVICE_NOTIFY_CALLBACK, DEVICE_NOTIFY_SERVICE_HANDLE, PowerSettingRegisterNotification, PowerSettingRegisterNotification function, base.powersettingregisternotification, powersetting/PowerSettingRegisterNotification, powrprof/PowerSettingRegisterNotification
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
 - PowerSettingRegisterNotification
 - powersetting/PowerSettingRegisterNotification
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
 - PowerSettingRegisterNotification
---

# PowerSettingRegisterNotification function


## -description

Registers to receive notification when a power setting changes.

## -parameters

### -param SettingGuid [in]

A GUID that represents the power setting.

### -param Flags [in]

Information about the recipient of the notification. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_SERVICE_HANDLE"></a><a id="device_notify_service_handle"></a><dl>
<dt><b>DEVICE_NOTIFY_SERVICE_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>Recipient</i> parameter is a handle to a service. Use the <a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> or <a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> function to obtain this handle.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_CALLBACK"></a><a id="device_notify_callback"></a><dl>
<dt><b>DEVICE_NOTIFY_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The <i>Recipient</i> parameter is a pointer to a callback function to call when the power setting changes. <i>Recipient</i> in this case is expected to be of type <i>PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</i>.

</td>
</tr>
</table>

### -param Recipient [in]

A handle to the recipient of the notifications.

### -param RegistrationHandle [out]

A handle to the registration. Use this handle to unregister for notifications.

## -returns

Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed.

## -remarks

Immediately after registration, the callback will be invoked with the current value of the power setting. If the registration occurs while the power setting is changing, you may receive multiple callbacks; the last callback is the most recent update.

## -see-also

<a href="/windows/desktop/Power/power-setting-guids">Power Setting GUIDs</a>



<a href="/windows/desktop/api/powersetting/nf-powersetting-powersettingunregisternotification">PowerSettingUnregisterNotification</a>
