---
UID: NF:adhoc.IDot11AdHocInterfaceNotificationSink.OnConnectionStatusChange
title: IDot11AdHocInterfaceNotificationSink::OnConnectionStatusChange
author: windows-sdk-content
description: Notifies the client that the connection status of the network associated with the NIC has changed.
old-location: nwifi\idot11adhocinterfacenotificationsink_onconnectionstatuschange.htm
tech.root: NativeWiFi
ms.assetid: a2116e44-e29b-4110-8794-ed161fdb534d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDot11AdHocInterfaceNotificationSink interface [NativeWIFI],OnConnectionStatusChange method, IDot11AdHocInterfaceNotificationSink.OnConnectionStatusChange, IDot11AdHocInterfaceNotificationSink::OnConnectionStatusChange, OnConnectionStatusChange, OnConnectionStatusChange method [NativeWIFI], OnConnectionStatusChange method [NativeWIFI],IDot11AdHocInterfaceNotificationSink interface, adhoc/IDot11AdHocInterfaceNotificationSink::OnConnectionStatusChange, nwifi.idot11adhocinterfacenotificationsink_onconnectionstatuschange
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocInterfaceNotificationSink.OnConnectionStatusChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDot11AdHocInterfaceNotificationSink::OnConnectionStatusChange


## -description


Notifies the client that the connection status of the network associated with the NIC has changed.


## -parameters




### -param eStatus

A pointer to a  <a href="https://msdn.microsoft.com/194179b9-9bd2-4c2f-ab22-c6b95eebfb43">DOT11_ADHOC_NETWORK_CONNECTION_STATUS</a> value that specifies the new connection state.


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



This notification is triggered when the connection status changes as a result of connection and disconnection requests issued by the current application. It is also triggered when other applications issue successful connection  and disconnection requests using the <a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a> methods or the <a href="https://msdn.microsoft.com/c1816d68-48b2-4d3d-a8c8-4a243a4b3f3b">Native Wifi functions</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab3fd026-32b4-48cb-aa10-37a084b5b08e">IDot11AdHocInterfaceNotificationSink</a>
 

 

