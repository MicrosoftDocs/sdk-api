---
UID: NF:adhoc.IDot11AdHocManagerNotificationSink.OnInterfaceAdd
title: IDot11AdHocManagerNotificationSink::OnInterfaceAdd (adhoc.h)
description: Notifies the client that a new network interface card (NIC) is active.
helpviewer_keywords: ["IDot11AdHocManagerNotificationSink interface [NativeWIFI]","OnInterfaceAdd method","IDot11AdHocManagerNotificationSink.OnInterfaceAdd","IDot11AdHocManagerNotificationSink::OnInterfaceAdd","OnInterfaceAdd","OnInterfaceAdd method [NativeWIFI]","OnInterfaceAdd method [NativeWIFI]","IDot11AdHocManagerNotificationSink interface","adhoc/IDot11AdHocManagerNotificationSink::OnInterfaceAdd","nwifi.idot11adhocmanagernotificationsink_oninterfaceadd"]
old-location: nwifi\idot11adhocmanagernotificationsink_oninterfaceadd.htm
tech.root: nwifi
ms.assetid: 1e2e390e-8587-4a00-9c04-b08ca026e348
ms.date: 12/05/2018
ms.keywords: IDot11AdHocManagerNotificationSink interface [NativeWIFI],OnInterfaceAdd method, IDot11AdHocManagerNotificationSink.OnInterfaceAdd, IDot11AdHocManagerNotificationSink::OnInterfaceAdd, OnInterfaceAdd, OnInterfaceAdd method [NativeWIFI], OnInterfaceAdd method [NativeWIFI],IDot11AdHocManagerNotificationSink interface, adhoc/IDot11AdHocManagerNotificationSink::OnInterfaceAdd, nwifi.idot11adhocmanagernotificationsink_oninterfaceadd
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
 - IDot11AdHocManagerNotificationSink::OnInterfaceAdd
 - adhoc/IDot11AdHocManagerNotificationSink::OnInterfaceAdd
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
 - IDot11AdHocManagerNotificationSink.OnInterfaceAdd
---

# IDot11AdHocManagerNotificationSink::OnInterfaceAdd


## -description

Notifies the client that a new network interface card (NIC) is active.

## -parameters

### -param pIAdHocInterface [in]

A pointer to an <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface">IDot11AdHocInterface</a> interface that represents the activated NIC.

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