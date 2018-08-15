---
UID: NF:netioapi.CancelMibChangeNotify2
title: CancelMibChangeNotify2 function
author: windows-sdk-content
description: Deregisters for change notifications for IP interface changes, IP address changes, IP route changes, Teredo port changes, and when the unicast IP address table is stable and can be retrieved.
old-location: iphlp\cancelmibchangenotify2.htm
old-project: iphlp
ms.assetid: 81492118-7513-49a2-9c61-3ecfaf84cc2d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CancelMibChangeNotify2, CancelMibChangeNotify2 function [IP Helper], iphlp.cancelmibchangenotify2, netioapi/CancelMibChangeNotify2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.redist: 
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
tech.root: 
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - CancelMibChangeNotify2
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>CancelMibChangeNotify2</b> function is defined on Windows Vista and later. 

The  
<b>CancelMibChangeNotify2</b> function deregisters for a change notification previously requested for IP interface changes, IP  address changes, IP route changes, or Teredo port changes on  a local computer. These requests are made  by calling <a href="https://msdn.microsoft.com/745128cf-7737-4f95-9712-26e0f6ae39b4">NotifyIpInterfaceChange</a>, <a href="https://msdn.microsoft.com/56945aa2-ca1e-44b3-9765-d862978a9dbe">NotifyUnicastIpAddressChange</a>, <a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a>,  or <a href="https://msdn.microsoft.com/c0c23531-7629-41c9-acf2-9d2f5e98e02c">NotifyTeredoPortChange</a>. The  
<b>CancelMibChangeNotify2</b> function also cancels a previous request to be notified when the unicast IP address table is stable on a local computer and can be  retrieved. This request is made by calling the <a href="https://msdn.microsoft.com/80d10088-79ef-41fd-add7-994d2a780ddb">NotifyStableUnicastIpAddressTable</a> function. 

The <i>NotificationHandle</i> parameter returned to these notification functions is passed to <b>CancelMibChangeNotify2</b> to deregister for notifications or cancel a pending request to retrieve the stable unicast IP address table.

An application cannot make a call to the <b>CancelMibChangeNotify2</b> function from the context of the thread which is currently executing the notification callback function for the same <i>NotificationHandle</i> parameter. Otherwise, the thread executing that callback will result in deadlock. So the <b>CancelMibChangeNotify2</b> function must not be called directly as part of the notification callback routine. In a more general situation, a thread that executes the <b>CancelMibChangeNotify2</b> function cannot own a resource on which the thread that executes a notification callback operation would wait because it would result in a similar deadlock. The <b>CancelMibChangeNotify2</b> function should be called from a different thread, on which the thread that receives the notification callback doesn’t have dependencies on.




## -see-also




<a href="https://msdn.microsoft.com/745128cf-7737-4f95-9712-26e0f6ae39b4">NotifyIpInterfaceChange</a>



<a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/80d10088-79ef-41fd-add7-994d2a780ddb">NotifyStableUnicastIpAddressTable</a>



<a href="https://msdn.microsoft.com/c0c23531-7629-41c9-acf2-9d2f5e98e02c">NotifyTeredoPortChange</a>



<a href="https://msdn.microsoft.com/56945aa2-ca1e-44b3-9765-d862978a9dbe">NotifyUnicastIpAddressChange</a>
 

 

