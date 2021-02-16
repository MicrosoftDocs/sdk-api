---
UID: NF:adhoc.IDot11AdHocManagerNotificationSink.OnNetworkAdd
title: IDot11AdHocManagerNotificationSink::OnNetworkAdd (adhoc.h)
description: Notifies the client that a new wireless ad hoc network destination is in range and available for connection.
helpviewer_keywords: ["IDot11AdHocManagerNotificationSink interface [NativeWIFI]","OnNetworkAdd method","IDot11AdHocManagerNotificationSink.OnNetworkAdd","IDot11AdHocManagerNotificationSink::OnNetworkAdd","OnNetworkAdd","OnNetworkAdd method [NativeWIFI]","OnNetworkAdd method [NativeWIFI]","IDot11AdHocManagerNotificationSink interface","adhoc/IDot11AdHocManagerNotificationSink::OnNetworkAdd","nwifi.idot11adhocmanagernotificationsink_onnetworkadd"]
old-location: nwifi\idot11adhocmanagernotificationsink_onnetworkadd.htm
tech.root: nwifi
ms.assetid: 28cca237-31a5-4018-a382-17d0a13a254b
ms.date: 12/05/2018
ms.keywords: IDot11AdHocManagerNotificationSink interface [NativeWIFI],OnNetworkAdd method, IDot11AdHocManagerNotificationSink.OnNetworkAdd, IDot11AdHocManagerNotificationSink::OnNetworkAdd, OnNetworkAdd, OnNetworkAdd method [NativeWIFI], OnNetworkAdd method [NativeWIFI],IDot11AdHocManagerNotificationSink interface, adhoc/IDot11AdHocManagerNotificationSink::OnNetworkAdd, nwifi.idot11adhocmanagernotificationsink_onnetworkadd
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDot11AdHocManagerNotificationSink::OnNetworkAdd
 - adhoc/IDot11AdHocManagerNotificationSink::OnNetworkAdd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocManagerNotificationSink.OnNetworkAdd
---

# IDot11AdHocManagerNotificationSink::OnNetworkAdd


## -description

Notifies the client that a new wireless ad hoc network destination is in range and available for connection.

## -parameters

### -param pIAdHocNetwork [in]

A pointer to an <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a> interface that represents the new network.

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

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink">IDot11AdHocManagerNotificationSink</a>