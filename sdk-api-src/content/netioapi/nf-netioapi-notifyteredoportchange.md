---
UID: NF:netioapi.NotifyTeredoPortChange
title: NotifyTeredoPortChange function (netioapi.h)
description: Registers to be notified for changes to the UDP port number used by the Teredo client for the Teredo service port on a local computer.
helpviewer_keywords: ["NotifyTeredoPortChange","NotifyTeredoPortChange function [IP Helper]","iphlp.notifyteredoportchange","netioapi/NotifyTeredoPortChange"]
old-location: iphlp\notifyteredoportchange.htm
tech.root: IpHlp
ms.assetid: c0c23531-7629-41c9-acf2-9d2f5e98e02c
ms.date: 12/05/2018
ms.keywords: NotifyTeredoPortChange, NotifyTeredoPortChange function [IP Helper], iphlp.notifyteredoportchange, netioapi/NotifyTeredoPortChange
req.header: netioapi.h
req.include-header: Iphlpapi.h
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NotifyTeredoPortChange
 - netioapi/NotifyTeredoPortChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - NotifyTeredoPortChange
---

# NotifyTeredoPortChange function


## -description

The 
<b>NotifyTeredoPortChange</b> function  registers to be notified for changes to the UDP port number used by the Teredo client for the Teredo service port on  a local computer.

## -parameters

### -param Callback [in]

A pointer to the function to call when a Teredo client port change occurs. This function will be invoked
        when a Teredo port change notification is received.

### -param CallerContext [in]

A user context passed to the callback function specified in the <i>Callback</i> parameter when a Teredo port change  notification is received.

### -param InitialNotification [in]

A value that indicates whether the callback should be invoked
        immediately after registration for change notification completes. This initial notification does not indicate a change occurred to the Teredo client port. The purpose of this parameter to provide confirmation that the callback is registered.

### -param NotificationHandle [in, out]

A pointer used to return a handle that can be later used to
        deregister the change notification. On success, a notification handle is returned in this parameter. If an error occurs, <b>NULL</b> is returned.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An internal error occurred where an invalid handle was encountered. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>Callback</i> parameter is a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>NotifyTeredoPortChange</b> function is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-getteredoport">GetTeredoPort</a> function can be used to retrieve the initial UDP port number used by the Teredo client for the Teredo service port. 

The Teredo port is dynamic and can change any time the Teredo client is restarted on the local computer. An application can  register to be notified when the Teredo service port changes by calling the <b>NotifyTeredoPortChange</b> function. 

The invocation of the callback function specified in the <i>Callback</i> parameter is serialized. The callback function should be defined as a function of type <b>VOID</b>. The parameters passed to the callback function include the following:

<table>
<tr>
<th>Parameter</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="IN_PVOID_CallerContext"></a><a id="in_pvoid_callercontext"></a><a id="IN_PVOID_CALLERCONTEXT"></a>IN PVOID CallerContext

</td>
<td width="60%">
The <i>CallerContext</i> parameter passed to the <b>NotifyTeredoPortChange</b> function when registering for notifications.

</td>
</tr>
<tr>
<td width="40%">
<a id="IN_USHORT_Port"></a><a id="in_ushort_port"></a><a id="IN_USHORT_PORT"></a>IN USHORT Port

</td>
<td width="60%">
The UDP port number currently used by the Teredo client. This parameter is <b>zero</b> when the <b>MIB_NOTIFICATION_TYPE</b> value passed in the <i>NotificationType</i> parameter to the callback function is set to <b>MibInitialNotification</b>. This can only occur if the <i>InitialNotification</i> parameter passed to <b>NotifyTeredoPortChange</b> was set to <b>TRUE</b> when registering for notifications.

</td>
</tr>
<tr>
<td width="40%">
<a id="IN_MIB_NOTIFICATION_TYPE_NotificationType"></a><a id="in_mib_notification_type_notificationtype"></a><a id="IN_MIB_NOTIFICATION_TYPE_NOTIFICATIONTYPE"></a>IN MIB_NOTIFICATION_TYPE NotificationType

</td>
<td width="60%">
The notification type. This member can be one of the values from the <a href="/windows/desktop/api/netioapi/ne-netioapi-mib_notification_type">MIB_NOTIFICATION_TYPE</a> enumeration type defined in the <i>Netioapi.h</i> header file.

</td>
</tr>
</table>
 



The callback function specified in the <i>Callback</i> parameter must be implemented in the same process as the application calling the <b>NotifyTeredoPortChange</b> function. If the callback function is in a separate DLL, then the DLL should be loaded before calling the <b>NotifyTeredoPortChange</b> function to register for change notifications. 

Once the <b>NotifyTeredoPortChange</b> function is called to register for change notifications, these notifications will continue to be sent until the application deregisters for change notifications or the application terminates. If the application terminates, the system will automatically deregister any registration for change notifications. It is still recommended that an application explicitly deregister for change notifications before it terminates.  

Any registration for change notifications does not persist across a system shut down or reboot.

To deregister for change notifications, call the  <a href="/windows/desktop/api/netioapi/nf-netioapi-cancelmibchangenotify2">CancelMibChangeNotify2</a> function passing the <i>NotificationHandle</i> parameter returned by  <b>NotifyTeredoPortChange</b>. 

An application cannot make a call to the <a href="/windows/desktop/api/netioapi/nf-netioapi-cancelmibchangenotify2">CancelMibChangeNotify2</a> function from the context of the thread which is currently executing the notification callback function for the same <i>NotificationHandle</i> parameter. Otherwise, the thread executing that callback will result in deadlock. So the <b>CancelMibChangeNotify2</b> function must not be called directly as part of the notification callback routine. In a more general situation, a thread that executes the <b>CancelMibChangeNotify2</b> function cannot own a resource on which the thread that executes a notification callback operation would wait because it would result in a similar deadlock. The <b>CancelMibChangeNotify2</b> function should be called from a different thread, on which the thread that receives the notification callback doesn’t have dependencies on.

The Teredo client also uses static UDP port 3544 for listening to multicast traffic sent on multicast IPv4 address 224.0.0.253 as defined in RFC 4380. For more information, see <a href="https://www.ietf.org/rfc/rfc4380.txt">http://www.ietf.org/rfc/rfc4380.txt</a>.

The <b>NotifyTeredoPortChange</b> function is used primarily by firewall applications in order to configure the appropriate exceptions to allow incoming and outgoing Teredo traffic. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable">NotifyStableUnicastIpAddressTable</a> function is used primarily by applications that use the Teredo client.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-cancelmibchangenotify2">CancelMibChangeNotify2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getteredoport">GetTeredoPort</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable">NotifyStableUnicastIpAddressTable</a>