---
UID: NF:winuser.RegisterPowerSettingNotification
title: RegisterPowerSettingNotification function (winuser.h)
description: Registers the application to receive power setting notifications for the specific power setting event.
helpviewer_keywords: ["DEVICE_NOTIFY_SERVICE_HANDLE","DEVICE_NOTIFY_WINDOW_HANDLE","RegisterPowerSettingNotification","RegisterPowerSettingNotification function","base.registerpowersettingnotification","winuser/RegisterPowerSettingNotification"]
old-location: base\registerpowersettingnotification.htm
tech.root: base
ms.assetid: e072222e-da66-4b36-a38f-f4b618eaa391
ms.date: 12/05/2018
ms.keywords: DEVICE_NOTIFY_SERVICE_HANDLE, DEVICE_NOTIFY_WINDOW_HANDLE, RegisterPowerSettingNotification, RegisterPowerSettingNotification function, base.registerpowersettingnotification, winuser/RegisterPowerSettingNotification
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
 - RegisterPowerSettingNotification
 - winuser/RegisterPowerSettingNotification
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
 - RegisterPowerSettingNotification
req.apiset: ext-ms-win-ntuser-powermanagement-l1-1-0 (introduced in Windows 8)
---

# RegisterPowerSettingNotification function


## -description

Registers the application to receive power setting notifications for the specific power setting event.

## -parameters

### -param hRecipient [in]

Handle indicating where the power setting notifications are to be sent. For interactive applications, the 
     <i>Flags</i> parameter should be zero, and the <i>hRecipient</i> parameter 
     should be a window handle. For services, the <i>Flags</i> parameter should be one, and the 
     <i>hRecipient</i> parameter should be a <b>SERVICE_STATUS_HANDLE</b> 
     as returned from 
     <a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a>.

### -param PowerSettingGuid [in]

The <b>GUID</b> of the power setting for which notifications are to be sent. For more information see <a href="/windows/desktop/Power/registering-for-power-events">Registering for Power 
      Events</a>.

### -param Flags [in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_WINDOW_HANDLE"></a><a id="device_notify_window_handle"></a><dl>
<dt><b>DEVICE_NOTIFY_WINDOW_HANDLE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Notifications are sent using <a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a> 
       messages with a <i>wParam</i> parameter of 
       <a href="/windows/desktop/Power/pbt-powersettingchange">PBT_POWERSETTINGCHANGE</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_SERVICE_HANDLE"></a><a id="device_notify_service_handle"></a><dl>
<dt><b>DEVICE_NOTIFY_SERVICE_HANDLE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Notifications are sent to the <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> callback 
       function with a <i>dwControl</i> parameter of 
       <b>SERVICE_CONTROL_POWEREVENT</b> and a <i>dwEventType</i> of 
       <a href="/windows/desktop/Power/pbt-powersettingchange">PBT_POWERSETTINGCHANGE</a>.

</td>
</tr>
</table>

## -returns

Returns a notification handle for unregistering for power notifications. If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/Power/registering-for-power-events">Registering for Power Events</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unregisterpowersettingnotification">UnregisterPowerSettingNotification</a>
