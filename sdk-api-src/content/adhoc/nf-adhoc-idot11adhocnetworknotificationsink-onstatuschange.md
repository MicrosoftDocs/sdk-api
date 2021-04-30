---
UID: NF:adhoc.IDot11AdHocNetworkNotificationSink.OnStatusChange
title: IDot11AdHocNetworkNotificationSink::OnStatusChange (adhoc.h)
description: Notifies the client that the connection status of the network has changed.
helpviewer_keywords: ["IDot11AdHocNetworkNotificationSink interface [NativeWIFI]","OnStatusChange method","IDot11AdHocNetworkNotificationSink.OnStatusChange","IDot11AdHocNetworkNotificationSink::OnStatusChange","OnStatusChange","OnStatusChange method [NativeWIFI]","OnStatusChange method [NativeWIFI]","IDot11AdHocNetworkNotificationSink interface","adhoc/IDot11AdHocNetworkNotificationSink::OnStatusChange","nwifi.idot11adhocnetworknotificationsink_onstatuschange"]
old-location: nwifi\idot11adhocnetworknotificationsink_onstatuschange.htm
tech.root: nwifi
ms.assetid: 795057bf-d97e-40b8-b242-5e3859ad3038
ms.date: 12/05/2018
ms.keywords: IDot11AdHocNetworkNotificationSink interface [NativeWIFI],OnStatusChange method, IDot11AdHocNetworkNotificationSink.OnStatusChange, IDot11AdHocNetworkNotificationSink::OnStatusChange, OnStatusChange, OnStatusChange method [NativeWIFI], OnStatusChange method [NativeWIFI],IDot11AdHocNetworkNotificationSink interface, adhoc/IDot11AdHocNetworkNotificationSink::OnStatusChange, nwifi.idot11adhocnetworknotificationsink_onstatuschange
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
 - IDot11AdHocNetworkNotificationSink::OnStatusChange
 - adhoc/IDot11AdHocNetworkNotificationSink::OnStatusChange
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
 - IDot11AdHocNetworkNotificationSink.OnStatusChange
---

# IDot11AdHocNetworkNotificationSink::OnStatusChange


## -description

Notifies the client that the connection status of the network has changed.

## -parameters

### -param eStatus

A <a href="/windows/win32/api/adhoc/ne-adhoc-dot11_adhoc_network_connection_status">DOT11_ADHOC_NETWORK_CONNECTION_STATUS</a> value that specifies the updated connection status.

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

This notification is triggered when the connection status changes as a result of connection and disconnection requests issued by the current application. It is also triggered when other applications issue successful connection  and disconnection requests using the <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a> methods or the <a href="/windows/desktop/NativeWiFi/native-wifi-functions">Native Wifi functions</a>. Connection and disconnection requests triggered by the user interface will also trigger the <b>OnStatusChange</b> notification.

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink">IDot11AdHocNetworkNotificationSink</a>