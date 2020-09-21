---
UID: NF:adhoc.IDot11AdHocNetworkNotificationSink.OnConnectFail
title: IDot11AdHocNetworkNotificationSink::OnConnectFail (adhoc.h)
description: Notifies the client that a connection attempt failed.
helpviewer_keywords: ["IDot11AdHocNetworkNotificationSink interface [NativeWIFI]","OnConnectFail method","IDot11AdHocNetworkNotificationSink.OnConnectFail","IDot11AdHocNetworkNotificationSink::OnConnectFail","OnConnectFail","OnConnectFail method [NativeWIFI]","OnConnectFail method [NativeWIFI]","IDot11AdHocNetworkNotificationSink interface","adhoc/IDot11AdHocNetworkNotificationSink::OnConnectFail","nwifi.idot11adhocnetworknotificationsink_onconnectfail"]
old-location: nwifi\idot11adhocnetworknotificationsink_onconnectfail.htm
tech.root: nwifi
ms.assetid: b38143c8-4e90-4f5d-b9f5-15bd1fd7e1c5
ms.date: 12/05/2018
ms.keywords: IDot11AdHocNetworkNotificationSink interface [NativeWIFI],OnConnectFail method, IDot11AdHocNetworkNotificationSink.OnConnectFail, IDot11AdHocNetworkNotificationSink::OnConnectFail, OnConnectFail, OnConnectFail method [NativeWIFI], OnConnectFail method [NativeWIFI],IDot11AdHocNetworkNotificationSink interface, adhoc/IDot11AdHocNetworkNotificationSink::OnConnectFail, nwifi.idot11adhocnetworknotificationsink_onconnectfail
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
 - IDot11AdHocNetworkNotificationSink::OnConnectFail
 - adhoc/IDot11AdHocNetworkNotificationSink::OnConnectFail
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
 - IDot11AdHocNetworkNotificationSink.OnConnectFail
---

# IDot11AdHocNetworkNotificationSink::OnConnectFail


## -description

Notifies the client that a connection attempt failed. The connection attempt may have been initiated by the client itself or by another application using the <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a> methods or the <a href="/windows/desktop/NativeWiFi/native-wifi-functions">Native Wifi functions</a>.

## -parameters

### -param eFailReason

A <a href="/windows/desktop/api/adhoc/ne-adhoc-dot11_adhoc_connect_fail_reason">DOT11_ADHOC_CONNECT_FAIL_REASON</a> value that specifies the reason the connection attempt failed.

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

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink">IDot11AdHocNetworkNotificationSink</a>