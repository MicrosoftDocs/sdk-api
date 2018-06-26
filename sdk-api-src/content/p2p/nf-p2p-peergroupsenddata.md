---
UID: NF:p2p.PeerGroupSendData
title: PeerGroupSendData function
author: windows-sdk-content
description: The PeerGroupSendData function sends data to a member over a neighbor or direct connection.
old-location: p2p\peergroupsenddata.htm
old-project: P2PSdk
ms.assetid: 8dcc484d-2b96-4186-990d-c32b7b254d91
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerGroupSendData, PeerGroupSendData function [Peer Networking], p2p.peergroupsenddata, p2p/PeerGroupSendData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerGroupSendData
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerGroupSendData function


## -description



      The <b>PeerGroupSendData</b> function sends data to a member over a neighbor or direct connection.


## -parameters




### -param hGroup [in]

Handle to the group that contains both members of a connection. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param ullConnectionId [in]

Unsigned 64-bit integer that contains the ID of the connection that  hosts the data transmission. A connection ID is obtained by calling <a href="https://msdn.microsoft.com/a3c52754-91b0-4722-a459-87c70b3ab9ad">PeerGroupOpenDirectConnection</a>. This parameter is required.


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
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



To receive data, the receiving peer must have registered for the <b>PEER_GROUP_EVENT_INCOMING_DATA</b> peer event.




## -see-also




<a href="https://msdn.microsoft.com/56b47743-f205-407b-80f2-03e3c9b78be1">PeerGroupCloseDirectConnection</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/a3c52754-91b0-4722-a459-87c70b3ab9ad">PeerGroupOpenDirectConnection</a>
 

 

