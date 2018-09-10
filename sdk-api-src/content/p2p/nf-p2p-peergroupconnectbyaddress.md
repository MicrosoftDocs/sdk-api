---
UID: NF:p2p.PeerGroupConnectByAddress
title: PeerGroupConnectByAddress function
author: windows-sdk-content
description: Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.
old-location: p2p\peergroupconnectbyaddress.htm
tech.root: p2psdk
ms.assetid: 44885110-fcb1-402a-86c6-1229b087165b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerGroupConnectByAddress, PeerGroupConnectByAddress function [Peer Networking], p2p.peergroupconnectbyaddress, p2p/PeerGroupConnectByAddress
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerGroupConnectByAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGroupConnectByAddress function


## -description


The <b>PeerGroupConnectByAddress</b> function  attempts to connect to the peer group that other peers with known IPv6 addresses are participating in. After this function is  called successfully, a peer can communicate with other members of the peer group.


## -parameters




### -param hGroup [in]

Handle to the peer group  to which a peer intends to connect. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>,<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>, or <a href="https://msdn.microsoft.com/aff8a462-a4cf-462b-a641-b1573311037b">PeerGroupPasswordJoin</a> function. This parameter is required.


### -param cAddresses [in]

The total number of <a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structures pointed to by <i>pAddresses</i>.


### -param pAddresses [in]

Pointer to a list of <a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structures that specify the endpoints of peers participating in the group.


## -returns



Returns S_OK if the operation succeeds. Otherwise, the function returns  the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
 

Cryptography-specific errors may be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



If  a time-out value for PeerGroupConnectByAddress is not provided in the application, encountering a failure will cause the application to hang.  A time-out value  of 30 seconds is recommended.




## -see-also




<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a>



<a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/aff8a462-a4cf-462b-a641-b1573311037b">PeerGroupPasswordJoin</a>
 

 

