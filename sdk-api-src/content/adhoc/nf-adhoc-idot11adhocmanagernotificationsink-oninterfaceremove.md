---
UID: NF:adhoc.IDot11AdHocManagerNotificationSink.OnInterfaceRemove
title: IDot11AdHocManagerNotificationSink::OnInterfaceRemove (adhoc.h)
description: Notifies the client that a network interface card (NIC) has become inactive.
helpviewer_keywords: ["IDot11AdHocManagerNotificationSink interface [NativeWIFI]","OnInterfaceRemove method","IDot11AdHocManagerNotificationSink.OnInterfaceRemove","IDot11AdHocManagerNotificationSink::OnInterfaceRemove","OnInterfaceRemove","OnInterfaceRemove method [NativeWIFI]","OnInterfaceRemove method [NativeWIFI]","IDot11AdHocManagerNotificationSink interface","adhoc/IDot11AdHocManagerNotificationSink::OnInterfaceRemove","nwifi.idot11adhocmanagernotificationsink_oninterfaceremove"]
old-location: nwifi\idot11adhocmanagernotificationsink_oninterfaceremove.htm
tech.root: nwifi
ms.assetid: ac62c211-9886-4c09-8867-32ce9763c2fc
ms.date: 12/05/2018
ms.keywords: IDot11AdHocManagerNotificationSink interface [NativeWIFI],OnInterfaceRemove method, IDot11AdHocManagerNotificationSink.OnInterfaceRemove, IDot11AdHocManagerNotificationSink::OnInterfaceRemove, OnInterfaceRemove, OnInterfaceRemove method [NativeWIFI], OnInterfaceRemove method [NativeWIFI],IDot11AdHocManagerNotificationSink interface, adhoc/IDot11AdHocManagerNotificationSink::OnInterfaceRemove, nwifi.idot11adhocmanagernotificationsink_oninterfaceremove
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
 - IDot11AdHocManagerNotificationSink::OnInterfaceRemove
 - adhoc/IDot11AdHocManagerNotificationSink::OnInterfaceRemove
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
 - IDot11AdHocManagerNotificationSink.OnInterfaceRemove
---

# IDot11AdHocManagerNotificationSink::OnInterfaceRemove


## -description

Notifies the client that a network interface card (NIC) has become inactive.

## -parameters

### -param Signature [in]

A pointer to a signature that uniquely identifies the inactive NIC. For more information about signatures, see <a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-getdevicesignature">IDot11AdHocInterface::GetDeviceSignature</a>.

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