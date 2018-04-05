---
UID: NF:adhoc.IDot11AdHocNetworkNotificationSink.OnStatusChange
title: IDot11AdHocNetworkNotificationSink::OnStatusChange method
author: windows-driver-content
description: Notifies the client that the connection status of the network has changed.
old-location: nwifi\idot11adhocnetworknotificationsink_onstatuschange.htm
old-project: NativeWiFi
ms.assetid: 795057bf-d97e-40b8-b242-5e3859ad3038
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IDot11AdHocNetworkNotificationSink, IDot11AdHocNetworkNotificationSink interface [NativeWIFI], OnStatusChange method, IDot11AdHocNetworkNotificationSink::OnStatusChange, OnStatusChange method [NativeWIFI], OnStatusChange method [NativeWIFI], IDot11AdHocNetworkNotificationSink interface, OnStatusChange,IDot11AdHocNetworkNotificationSink.OnStatusChange, adhoc/IDot11AdHocNetworkNotificationSink::OnStatusChange, nwifi.idot11adhocnetworknotificationsink_onstatuschange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	adhoc.h
api_name:
-	IDot11AdHocNetworkNotificationSink.OnStatusChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocNetworkNotificationSink::OnStatusChange method


## -description


Notifies the client that the connection status of the network has changed.


## -parameters




### -param eStatus

A <a href="https://msdn.microsoft.com/194179b9-9bd2-4c2f-ab22-c6b95eebfb43">DOT11_ADHOC_NETWORK_CONNECTION_STATUS</a> value that specifies the updated connection status.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -remarks



This notification is triggered when the connection status changes as a result of connection and disconnection requests issued by the current application. It is also triggered when other applications issue successful connection  and disconnection requests using the <a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a> methods or the <a href="https://msdn.microsoft.com/c1816d68-48b2-4d3d-a8c8-4a243a4b3f3b">Native Wifi functions</a>. Connection and disconnection requests triggered by the user interface will also trigger the <b>OnStatusChange</b> notification.




## -see-also




<a href="https://msdn.microsoft.com/54a45431-8036-4a3f-9558-467a1efab6bb">IDot11AdHocNetworkNotificationSink</a>
 

 

