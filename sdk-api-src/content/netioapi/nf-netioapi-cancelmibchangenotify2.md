---
UID: NF:netioapi.CancelMibChangeNotify2
title: CancelMibChangeNotify2 function (netioapi.h)
description: Deregisters for change notifications for IP interface changes, IP address changes, IP route changes, Teredo port changes, and when the unicast IP address table is stable and can be retrieved.
helpviewer_keywords: ["CancelMibChangeNotify2","CancelMibChangeNotify2 function [IP Helper]","iphlp.cancelmibchangenotify2","netioapi/CancelMibChangeNotify2"]
old-location: iphlp\cancelmibchangenotify2.htm
tech.root: IpHlp
ms.assetid: 81492118-7513-49a2-9c61-3ecfaf84cc2d
ms.date: 12/05/2018
ms.keywords: CancelMibChangeNotify2, CancelMibChangeNotify2 function [IP Helper], iphlp.cancelmibchangenotify2, netioapi/CancelMibChangeNotify2
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - CancelMibChangeNotify2
 - netioapi/CancelMibChangeNotify2
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
 - CancelMibChangeNotify2
---

# CancelMibChangeNotify2 function


## -description

The <b>CancelMibChangeNotify2</b> function deregisters for change notifications for IP interface changes, IP address changes, IP route changes, Teredo port changes, and when the unicast IP address table is stable and can be retrieved.

## -parameters

### -param NotificationHandle [in]

The handle returned from a notification 
        registration or retrieval function to indicate which notification to cancel.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>NotificationHandle</i> parameter was  a <b>NULL</b> pointer.

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

The <b>CancelMibChangeNotify2</b> function is defined on Windows Vista and later. 

The  
<b>CancelMibChangeNotify2</b> function deregisters for a change notification previously requested for IP interface changes, IP  address changes, IP route changes, or Teredo port changes on  a local computer. These requests are made  by calling <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a>, <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>, <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyroutechange2">NotifyRouteChange2</a>,  or <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange">NotifyTeredoPortChange</a>. The  
<b>CancelMibChangeNotify2</b> function also cancels a previous request to be notified when the unicast IP address table is stable on a local computer and can be  retrieved. This request is made by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable">NotifyStableUnicastIpAddressTable</a> function. 

The <i>NotificationHandle</i> parameter returned to these notification functions is passed to <b>CancelMibChangeNotify2</b> to deregister for notifications or cancel a pending request to retrieve the stable unicast IP address table.

An application cannot make a call to the <b>CancelMibChangeNotify2</b> function from the context of the thread which is currently executing the notification callback function for the same <i>NotificationHandle</i> parameter. Otherwise, the thread executing that callback will result in deadlock. So the <b>CancelMibChangeNotify2</b> function must not be called directly as part of the notification callback routine. In a more general situation, a thread that executes the <b>CancelMibChangeNotify2</b> function cannot own a resource on which the thread that executes a notification callback operation would wait because it would result in a similar deadlock. The <b>CancelMibChangeNotify2</b> function should be called from a different thread, on which the thread that receives the notification callback doesn’t have dependencies on.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyroutechange2">NotifyRouteChange2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable">NotifyStableUnicastIpAddressTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange">NotifyTeredoPortChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>