---
UID: NF:adhoc.IDot11AdHocNetworkNotificationSink.OnConnectFail
title: IDot11AdHocNetworkNotificationSink::OnConnectFail
author: windows-sdk-content
description: Notifies the client that a connection attempt failed.
old-location: nwifi\idot11adhocnetworknotificationsink_onconnectfail.htm
tech.root: NativeWiFi
ms.assetid: b38143c8-4e90-4f5d-b9f5-15bd1fd7e1c5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDot11AdHocNetworkNotificationSink interface [NativeWIFI],OnConnectFail method, IDot11AdHocNetworkNotificationSink.OnConnectFail, IDot11AdHocNetworkNotificationSink::OnConnectFail, OnConnectFail, OnConnectFail method [NativeWIFI], OnConnectFail method [NativeWIFI],IDot11AdHocNetworkNotificationSink interface, adhoc/IDot11AdHocNetworkNotificationSink::OnConnectFail, nwifi.idot11adhocnetworknotificationsink_onconnectfail
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
 - IDot11AdHocNetworkNotificationSink.OnConnectFail
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDot11AdHocNetworkNotificationSink::OnConnectFail


## -description


Notifies the client that a connection attempt failed. The connection attempt may have been initiated by the client itself or by another application using the <a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a> methods or the <a href="https://msdn.microsoft.com/c1816d68-48b2-4d3d-a8c8-4a243a4b3f3b">Native Wifi functions</a>.


## -parameters




### -param eFailReason

A <a href="https://msdn.microsoft.com/ea95f0b8-14ce-40a6-b5a3-853c414c52af">DOT11_ADHOC_CONNECT_FAIL_REASON</a> value that specifies the reason the connection attempt failed.


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
 




## -see-also




<a href="https://msdn.microsoft.com/54a45431-8036-4a3f-9558-467a1efab6bb">IDot11AdHocNetworkNotificationSink</a>
 

 

