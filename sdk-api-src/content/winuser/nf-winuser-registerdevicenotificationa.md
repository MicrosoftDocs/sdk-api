---
UID: NF:winuser.RegisterDeviceNotificationA
title: RegisterDeviceNotificationA function (winuser.h)
description: Registers the device or type of device for which a window will receive notifications. (ANSI)
helpviewer_keywords: ["DEVICE_NOTIFY_ALL_INTERFACE_CLASSES", "DEVICE_NOTIFY_SERVICE_HANDLE", "DEVICE_NOTIFY_WINDOW_HANDLE", "RegisterDeviceNotificationA", "winuser/RegisterDeviceNotificationA"]
old-location: base\registerdevicenotification.htm
tech.root: base
ms.assetid: 82094d95-9af3-4222-9c5e-ce2df9bab5e3
ms.date: 12/05/2018
ms.keywords: DEVICE_NOTIFY_ALL_INTERFACE_CLASSES, DEVICE_NOTIFY_SERVICE_HANDLE, DEVICE_NOTIFY_WINDOW_HANDLE, RegisterDeviceNotification, RegisterDeviceNotification function, RegisterDeviceNotificationA, RegisterDeviceNotificationW, _win32_registerdevicenotification, base.registerdevicenotification, winuser/RegisterDeviceNotification, winuser/RegisterDeviceNotificationA, winuser/RegisterDeviceNotificationW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterDeviceNotificationW (Unicode) and RegisterDeviceNotificationA (ANSI)
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
 - RegisterDeviceNotificationA
 - winuser/RegisterDeviceNotificationA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - RegisterDeviceNotification
 - RegisterDeviceNotificationA
 - RegisterDeviceNotificationW
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# RegisterDeviceNotificationA function


## -description

Registers the device or type of device for which a window will receive notifications.

> [!NOTE]
> You can use <a href="/windows/win32/api/cfgmgr32/nf-cfgmgr32-cm_register_notification">CM_Register_Notification</a> instead of <b>RegisterDeviceNotification</b> if your code targets Windows 8 or newer versions of Windows. The advantage of <b>CM_Register_Notification</b> is that it does not require a window handle to work.

## -parameters

### -param hRecipient [in]

A handle to the window or service that will receive device events for the devices specified in the 
       <i>NotificationFilter</i> parameter. The same window handle can be used in multiple calls to 
       <b>RegisterDeviceNotification</b>.

Services can specify either a window handle or service status handle.

### -param NotificationFilter [in]

A pointer to a block of data that specifies the type of device for which notifications should be sent. This 
      block always begins with the <a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a> 
      structure. The data following this header is dependent on the value of the 
      <b>dbch_devicetype</b> member, which can be 
      <b>DBT_DEVTYP_DEVICEINTERFACE</b> or <b>DBT_DEVTYP_HANDLE</b>. For more 
      information, see Remarks.

### -param Flags [in]

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_WINDOW_HANDLE"></a><a id="device_notify_window_handle"></a><dl>
<dt><b>DEVICE_NOTIFY_WINDOW_HANDLE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The <i>hRecipient</i> parameter is a window handle.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_SERVICE_HANDLE"></a><a id="device_notify_service_handle"></a><dl>
<dt><b>DEVICE_NOTIFY_SERVICE_HANDLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <i>hRecipient</i> parameter is a service status handle.

</td>
</tr>
</table>
 

In addition, you can specify the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_ALL_INTERFACE_CLASSES"></a><a id="device_notify_all_interface_classes"></a><dl>
<dt><b>DEVICE_NOTIFY_ALL_INTERFACE_CLASSES</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Notifies the recipient of device interface events for all device interface classes. (The 
         <b>dbcc_classguid</b> member is ignored.)

This value can be used only if the <b>dbch_devicetype</b> member is 
         <b>DBT_DEVTYP_DEVICEINTERFACE</b>.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a device notification handle.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Applications send event notifications using the 
    <a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage">BroadcastSystemMessage</a> function. Any 
    application with a top-level window can receive basic notifications by processing the 
    <a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a> message. Applications can use the 
    <b>RegisterDeviceNotification</b> function to 
    register to receive device notifications.

Services can use the 
    <b>RegisterDeviceNotification</b> function to 
    register to receive device notifications. If a service specifies a window handle in the 
    <i>hRecipient</i> parameter, the notifications are sent to the window procedure. If 
    <i>hRecipient</i> is a service status handle, 
    <b>SERVICE_CONTROL_DEVICEEVENT</b> notifications are sent to the service control handler. For 
    more information about the service control handler, see 
    <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>.

Be sure to handle Plug and Play device events as quickly as possible. Otherwise, the system may become 
    unresponsive. If your event handler is to perform an operation that may block execution (such as I/O), it is best 
    to start another thread to perform the operation asynchronously.

Device notification handles returned by 
    <b>RegisterDeviceNotification</b> must be closed 
    by calling the 
    <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification">UnregisterDeviceNotification</a> function 
    when they are no longer needed.

The <a href="/windows/desktop/DevIO/dbt-devicearrival">DBT_DEVICEARRIVAL</a> and 
    <a href="/windows/desktop/DevIO/dbt-deviceremovecomplete">DBT_DEVICEREMOVECOMPLETE</a> events are 
    automatically broadcast to all top-level windows for port devices. Therefore, it is not necessary to call 
    <b>RegisterDeviceNotification</b> for ports, and 
    the function fails if the <b>dbch_devicetype</b> member is 
    <b>DBT_DEVTYP_PORT</b>. Volume notifications are also broadcast to top-level windows, so the 
    function fails if <b>dbch_devicetype</b> is <b>DBT_DEVTYP_VOLUME</b>. 
    OEM-defined devices are not used directly by the system, so the function fails if 
    <b>dbch_devicetype</b> is <b>DBT_DEVTYP_OEM</b>.


#### Examples

For an example, see 
     <a href="/windows/desktop/DevIO/registering-for-device-notification">Registering for device notification</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines RegisterDeviceNotification as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage">BroadcastSystemMessage</a>



<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a>



<a href="/windows/desktop/DevIO/device-management-functions">Device Management Functions</a>



<a href="/windows/desktop/DevIO/device-notifications">Device Notifications</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification">UnregisterDeviceNotification</a>



<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>
