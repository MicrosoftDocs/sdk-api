---
UID: NF:netioapi.NotifyIpInterfaceChange
title: NotifyIpInterfaceChange function (netioapi.h)
description: Registers to be notified for changes to all IP interfaces, IPv4 interfaces, or IPv6 interfaces on a local computer.
helpviewer_keywords: ["AF_INET","AF_INET6","AF_UNSPEC","NotifyIpInterfaceChange","NotifyIpInterfaceChange function [IP Helper]","iphlp.notifyipinterfacechange","netioapi/NotifyIpInterfaceChange"]
old-location: iphlp\notifyipinterfacechange.htm
tech.root: IpHlp
ms.assetid: 745128cf-7737-4f95-9712-26e0f6ae39b4
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, AF_UNSPEC, NotifyIpInterfaceChange, NotifyIpInterfaceChange function [IP Helper], iphlp.notifyipinterfacechange, netioapi/NotifyIpInterfaceChange
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
 - NotifyIpInterfaceChange
 - netioapi/NotifyIpInterfaceChange
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
 - NotifyIpInterfaceChange
---

# NotifyIpInterfaceChange function


## -description

The 
<b>NotifyIpInterfaceChange</b> function  registers to be notified for changes to all IP interfaces, IPv4 interfaces, or IPv6 interfaces on  a local computer.

## -parameters

### -param Family [in]

The address family on which to register for change notifications.

Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b>, <b>AF_INET6</b>, and <b>AF_UNSPEC</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The address family is unspecified. When this parameter is specified,  this function registers for both IPv4 and IPv6 change notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
 The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  this function register for only IPv4 change notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
 The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  this function registers for only IPv6 change notifications.

</td>
</tr>
</table>

### -param Callback [in]

A pointer to the function to call when a change occurs. This function will be invoked
        when an interface notification is received.

### -param CallerContext [in]

A user context passed to the callback function specified in the <i>Callback</i> parameter when an interface notification is received.

### -param InitialNotification [in]

A value that indicates whether the callback should be invoked
        immediately after registration for change notification completes. This initial notification does not indicate a change occurred to an IP interface. The purpose of this parameter to provide confirmation that the callback is registered.

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
An invalid parameter was passed to the function. This error is returned if the <i>Family</i> parameter was not either <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>.

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

The <b>NotifyIpInterfaceChange</b> function is defined on Windows Vista and later. 

The <i>Family</i> parameter must be set to either <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>. 

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
The <i>CallerContext</i> parameter passed to the <b>NotifyIpInterfaceChange</b> function when registering for notifications.

</td>
</tr>
<tr>
<td width="40%">
<a id="IN_PMIB_IPINTERFACE_ROW_Row_OPTIONAL"></a><a id="in_pmib_ipinterface_row_row_optional"></a><a id="IN_PMIB_IPINTERFACE_ROW_ROW_OPTIONAL"></a>IN PMIB_IPINTERFACE_ROW Row OPTIONAL

</td>
<td width="60%">
A pointer to the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> entry for the  interface that was changed. This parameter is a <b>NULL</b> pointer when the <b>MIB_NOTIFICATION_TYPE</b> value passed in the <i>NotificationType</i> parameter to the callback function is set to <b>MibInitialNotification</b>. This can only occur if the <i>InitialNotification</i> parameter passed to <b>NotifyIpInterfaceChange</b> was set to <b>TRUE</b> when registering for notifications.

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
 



The callback function specified in the <i>Callback</i> parameter must be implemented in the same process as the application calling the <b>NotifyIpInterfaceChange</b> function. If the callback function is in a separate DLL, then the DLL should be loaded before calling the <b>NotifyIpInterfaceChange</b> function to register for change notifications. 

When the callback function is received when a change occurs and the <i>Row</i> parameter is not <b>NULL</b>, the pointer to the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> structure passed in the <i>Row</i> parameter contains incomplete data. The  information returned in the <b>MIB_IPINTERFACE_ROW</b> structure is only enough information that an application can call the <a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a> function to query complete information on the IP interface that changed. When the callback function is received, an application should allocate a <b>MIB_IPINTERFACE_ROW</b> structure and initialize it with the <b>Family</b>,  <b>InterfaceLuid</b> and <b>InterfaceIndex</b> members in the <b>MIB_IPINTERFACE_ROW</b> structure pointed to by the <i>Row</i> parameter received. A pointer to this newly initialized <b>MIB_IPINTERFACE_ROW</b> structure should be passed to the <b>GetIpInterfaceEntry</b> function to retrieve complete information on the IP interface that was changed. 

The memory pointed to by the <i>Row</i> parameter used in the callback indications is managed by the operating system.  An application that receives a notification should never attempt to free the memory pointed to by the <i>Row</i> parameter. 

To deregister for change notifications, call the  <a href="/windows/desktop/api/netioapi/nf-netioapi-cancelmibchangenotify2">CancelMibChangeNotify2</a> function passing the <i>NotificationHandle</i> parameter returned by  <b>NotifyIpInterfaceChange</b>. 

An application cannot make a call to the <a href="/windows/desktop/api/netioapi/nf-netioapi-cancelmibchangenotify2">CancelMibChangeNotify2</a> function from the context of the thread which is currently executing the notification callback function for the same <i>NotificationHandle</i> parameter. Otherwise, the thread executing that callback will result in deadlock. So the <b>CancelMibChangeNotify2</b> function must not be called directly as part of the notification callback routine. In a more general situation, a thread that executes the <b>CancelMibChangeNotify2</b> function cannot own a resource on which the thread that executes a notification callback operation would wait because it would result in a similar deadlock. The <b>CancelMibChangeNotify2</b> function should be called from a different thread, on which the thread that receives the notification callback doesn’t have dependencies on.

Once the <b>NotifyIpInterfaceChange</b> function is called to register for change notifications, these notifications will continue to be sent until the application deregisters for change notifications or the application terminates. If the application terminates, the system will automatically deregister any registration for change notifications. It is still recommended that an application explicitly deregister for change notifications before it terminates.  

Any registration for change notifications does not persist across a system shut down or reboot.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-cancelmibchangenotify2">CancelMibChangeNotify2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifentry2">GetIfEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifstacktable">GetIfStackTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getinvertedifstacktable">GetInvertedIfStackTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeipinterfaceentry">InitializeIpInterfaceEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>



<a href="/windows/desktop/api/netioapi/ne-netioapi-mib_notification_type">MIB_NOTIFICATION_TYPE</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setipinterfaceentry">SetIpInterfaceEntry</a>