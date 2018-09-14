---
UID: NF:adhoc.IDot11AdHocManagerNotificationSink.OnNetworkRemove
title: IDot11AdHocManagerNotificationSink::OnNetworkRemove
author: windows-sdk-content
description: Notifies the client that a wireless ad hoc network destination is no longer available for connection.
old-location: nwifi\idot11adhocmanagernotificationsink_onnetworkremove.htm
tech.root: NativeWiFi
ms.assetid: 9f325b86-3aff-4344-a154-86b74a922372
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDot11AdHocManagerNotificationSink interface [NativeWIFI],OnNetworkRemove method, IDot11AdHocManagerNotificationSink.OnNetworkRemove, IDot11AdHocManagerNotificationSink::OnNetworkRemove, OnNetworkRemove, OnNetworkRemove method [NativeWIFI], OnNetworkRemove method [NativeWIFI],IDot11AdHocManagerNotificationSink interface, adhoc/IDot11AdHocManagerNotificationSink::OnNetworkRemove, nwifi.idot11adhocmanagernotificationsink_onnetworkremove
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
 - IDot11AdHocManagerNotificationSink.OnNetworkRemove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDot11AdHocManagerNotificationSink::OnNetworkRemove


## -description


Notifies the client that a wireless ad hoc network destination is no longer  available for connection.


## -parameters




### -param Signature [in]

A pointer to a signature that uniquely identifies the newly unavailable network. For more information about signatures, see <a href="https://msdn.microsoft.com/0a59a8bd-d2eb-48c6-8480-dc4dea335d22">IDot11AdHocNetwork::GetSignature</a>.


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
 

 

