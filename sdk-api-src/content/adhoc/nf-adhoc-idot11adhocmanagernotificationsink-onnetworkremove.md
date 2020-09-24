---
UID: NF:adhoc.IDot11AdHocManagerNotificationSink.OnNetworkRemove
title: IDot11AdHocManagerNotificationSink::OnNetworkRemove (adhoc.h)
description: Notifies the client that a wireless ad hoc network destination is no longer available for connection.
helpviewer_keywords: ["IDot11AdHocManagerNotificationSink interface [NativeWIFI]","OnNetworkRemove method","IDot11AdHocManagerNotificationSink.OnNetworkRemove","IDot11AdHocManagerNotificationSink::OnNetworkRemove","OnNetworkRemove","OnNetworkRemove method [NativeWIFI]","OnNetworkRemove method [NativeWIFI]","IDot11AdHocManagerNotificationSink interface","adhoc/IDot11AdHocManagerNotificationSink::OnNetworkRemove","nwifi.idot11adhocmanagernotificationsink_onnetworkremove"]
old-location: nwifi\idot11adhocmanagernotificationsink_onnetworkremove.htm
tech.root: nwifi
ms.assetid: 9f325b86-3aff-4344-a154-86b74a922372
ms.date: 12/05/2018
ms.keywords: IDot11AdHocManagerNotificationSink interface [NativeWIFI],OnNetworkRemove method, IDot11AdHocManagerNotificationSink.OnNetworkRemove, IDot11AdHocManagerNotificationSink::OnNetworkRemove, OnNetworkRemove, OnNetworkRemove method [NativeWIFI], OnNetworkRemove method [NativeWIFI],IDot11AdHocManagerNotificationSink interface, adhoc/IDot11AdHocManagerNotificationSink::OnNetworkRemove, nwifi.idot11adhocmanagernotificationsink_onnetworkremove
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
 - IDot11AdHocManagerNotificationSink::OnNetworkRemove
 - adhoc/IDot11AdHocManagerNotificationSink::OnNetworkRemove
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
 - IDot11AdHocManagerNotificationSink.OnNetworkRemove
---

# IDot11AdHocManagerNotificationSink::OnNetworkRemove


## -description

Notifies the client that a wireless ad hoc network destination is no longer  available for connection.

## -parameters

### -param Signature [in]

A pointer to a signature that uniquely identifies the newly unavailable network. For more information about signatures, see <a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getsignature">IDot11AdHocNetwork::GetSignature</a>.

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