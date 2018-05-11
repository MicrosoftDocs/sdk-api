---
UID: NF:p2p.PeerGroupOpenDirectConnection
title: PeerGroupOpenDirectConnection function
author: windows-driver-content
description: The PeerGroupOpenDirectConnection function establishes a direct connection with another peer in a peer group.
old-location: p2p\peergroupopendirectconnection.htm
old-project: P2PSdk
ms.assetid: a3c52754-91b0-4722-a459-87c70b3ab9ad
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerGroupOpenDirectConnection, PeerGroupOpenDirectConnection function [Peer Networking], p2p.peergroupopendirectconnection, p2p/PeerGroupOpenDirectConnection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerGroupOpenDirectConnection
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerGroupOpenDirectConnection function


## -description



      The <b>PeerGroupOpenDirectConnection</b> function establishes a direct connection with another peer in a peer group.


## -parameters




### -param hGroup [in]

Handle to the peer group that hosts the direct connection. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param pwzIdentity [in]

Pointer to a Unicode string that contains the identity   a peer  connects to. This parameter is required.


### -param pAddress [in]

Pointer to a <a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structure that contains the IPv6 address   the peer  connects to. This parameter is required.


### -param pullConnectionId [out]

Unsigned 64-bit integer that identifies the direct connection. This ID value cannot be assumed as valid until the <a href="https://msdn.microsoft.com/9c28eb24-f158-4313-9a7c-0f271013d03a">PEER_GROUP_EVENT_DIRECT_CONNECTION</a> event is raised and indicates that the connection has been accepted by the other peer. This parameter is required.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_CONNECT_SELF</b></dt>
</dl>
</td>
<td width="60%">
The connection failed because it was a loopback, that is, the connection is between a peer and itself.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. This is typically caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually. 


</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



Every direct connection opened with this function must be closed with <a href="https://msdn.microsoft.com/56b47743-f205-407b-80f2-03e3c9b78be1">PeerGroupCloseDirectConnection</a> when the exchange has finished. If the peer refuses a connection or if the connection fails, S_OK is returned. However, a <a href="https://msdn.microsoft.com/9c28eb24-f158-4313-9a7c-0f271013d03a">PEER_GROUP_EVENT_DIRECT_CONNECTION</a> event is generated, and  the corresponding <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT DATA</a> structure has the  <b>status</b> member of its component <a href="https://msdn.microsoft.com/0d73432c-c1e5-4fa9-a812-377b22a47440">PEER_EVENT_CONNECTION_CHANGE_DATA</a> structure set to PEER_CONNECTION_FAILED.




## -see-also




<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca"> PEER_ADDRESS</a>



<a href="https://msdn.microsoft.com/0d73432c-c1e5-4fa9-a812-377b22a47440">PEER_EVENT_CONNECTION_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT DATA</a>



<a href="https://msdn.microsoft.com/9c28eb24-f158-4313-9a7c-0f271013d03a">PEER_GROUP_EVENT_DIRECT_CONNECTION</a>



<a href="https://msdn.microsoft.com/56b47743-f205-407b-80f2-03e3c9b78be1">PeerGroupCloseDirectConnection</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/8dcc484d-2b96-4186-990d-c32b7b254d91">PeerGroupSendData</a>
 

 

