---
UID: NF:adhoc.IDot11AdHocManagerNotificationSink.OnNetworkAdd
title: IDot11AdHocManagerNotificationSink::OnNetworkAdd
author: windows-sdk-content
description: Notifies the client that a new wireless ad hoc network destination is in range and available for connection.
old-location: nwifi\idot11adhocmanagernotificationsink_onnetworkadd.htm
old-project: nativewifi
ms.assetid: 28cca237-31a5-4018-a382-17d0a13a254b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDot11AdHocManagerNotificationSink interface [NativeWIFI],OnNetworkAdd method, IDot11AdHocManagerNotificationSink.OnNetworkAdd, IDot11AdHocManagerNotificationSink::OnNetworkAdd, OnNetworkAdd, OnNetworkAdd method [NativeWIFI], OnNetworkAdd method [NativeWIFI],IDot11AdHocManagerNotificationSink interface, adhoc/IDot11AdHocManagerNotificationSink::OnNetworkAdd, nwifi.idot11adhocmanagernotificationsink_onnetworkadd
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocManagerNotificationSink.OnNetworkAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocManagerNotificationSink::OnNetworkAdd


## -description


Notifies the client that a new wireless ad hoc network destination is in range and available for connection.


## -parameters




### -param pIAdHocNetwork [in]

A pointer to an <a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a> interface that represents the new network.


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




<a href="https://msdn.microsoft.com/a79931ad-deeb-4e46-a051-80a57fe5935c">IDot11AdHocManagerNotificationSink</a>
 

 

