---
UID: NF:p2p.PeerGroupCloseDirectConnection
title: PeerGroupCloseDirectConnection function
author: windows-sdk-content
description: The PeerGroupCloseDirectConnection function closes a specific direct connection between two peers.
old-location: p2p\peergroupclosedirectconnection.htm
old-project: p2psdk
ms.assetid: 56b47743-f205-407b-80f2-03e3c9b78be1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerGroupCloseDirectConnection, PeerGroupCloseDirectConnection function [Peer Networking], p2p.peergroupclosedirectconnection, p2p/PeerGroupCloseDirectConnection
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
 - PeerGroupCloseDirectConnection
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerGroupCloseDirectConnection function


## -description


The <b>PeerGroupCloseDirectConnection</b> function closes a specific direct connection between two peers.


## -parameters




### -param hGroup [in]

Handle to the peer group that contains the peers involved in the direct connection. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param ullConnectionId [in]

Specifies the connection ID  to disconnect from. This parameter is required and has no default value.


## -returns



Returns S_OK if the operation succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_CONNECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A direct connection that matches the supplied connection ID cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer group is invalid.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/a3c52754-91b0-4722-a459-87c70b3ab9ad">PeerGroupOpenDirectConnection</a>
 

 

