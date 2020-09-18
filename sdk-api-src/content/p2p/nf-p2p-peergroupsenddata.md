---
UID: NF:p2p.PeerGroupSendData
title: PeerGroupSendData function (p2p.h)
description: The PeerGroupSendData function sends data to a member over a neighbor or direct connection.
helpviewer_keywords: ["PeerGroupSendData","PeerGroupSendData function [Peer Networking]","p2p.peergroupsenddata","p2p/PeerGroupSendData"]
old-location: p2p\peergroupsenddata.htm
tech.root: p2p
ms.assetid: 8dcc484d-2b96-4186-990d-c32b7b254d91
ms.date: 12/05/2018
ms.keywords: PeerGroupSendData, PeerGroupSendData function [Peer Networking], p2p.peergroupsenddata, p2p/PeerGroupSendData
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGroupSendData
 - p2p/PeerGroupSendData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerGroupSendData
---

# PeerGroupSendData function


## -description

The <b>PeerGroupSendData</b> function sends data to a member over a neighbor or direct connection.

## -parameters

### -param hGroup [in]

Handle to the group that contains both members of a connection. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param ullConnectionId [in]

Unsigned 64-bit integer that contains the ID of the connection that  hosts the data transmission. A connection ID is obtained by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopendirectconnection">PeerGroupOpenDirectConnection</a>. This parameter is required.

### -param pType [in]

Pointer to a <b>GUID</b> value that uniquely identifies the data being transmitted. This parameter is required.

### -param cbData [in]

Specifies the size of  the data in <i>pvData</i>, in bytes. This parameter is required.

### -param pvData [in]

Pointer to the block of data to send. The receiving application is responsible for parsing this data. This parameter is required.

## -returns

Returns <b>S_OK</b>  if the operation succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_CONNECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A connection with the ID specified in <i>ullConnectionId</i>  cannot be found.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

To receive data, the receiving peer must have registered for the <b>PEER_GROUP_EVENT_INCOMING_DATA</b> peer event.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupclosedirectconnection">PeerGroupCloseDirectConnection</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopendirectconnection">PeerGroupOpenDirectConnection</a>