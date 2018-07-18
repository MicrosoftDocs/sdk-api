---
UID: NF:p2p.PeerIdentityDelete
title: PeerIdentityDelete function
author: windows-sdk-content
description: The PeerIdentityDelete function permanently deletes a peer identity. This includes removing all certificates, private keys, and all group information associated with a specified peer identity.
old-location: p2p\peeridentitydelete.htm
old-project: P2PSdk
ms.assetid: 9738f6b1-cd88-4950-bab1-f97613a49e03
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PeerIdentityDelete, PeerIdentityDelete function [Peer Networking], p2p.peeridentitydelete, p2p/PeerIdentityDelete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
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
 - PeerIdentityDelete
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerIdentityDelete function


## -description



      The <b>PeerIdentityDelete</b> function permanently deletes a peer identity. This includes removing all certificates, private keys, and all group information associated with a specified peer identity.


## -parameters




### -param pwzIdentity [in]

Specifies a peer identity to delete.


## -returns



If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

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
The parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GROUPS_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The peer identity cannot be deleted because it has  peer groups associated with it.   All peer groups associated with the specified identity must be deleted by using   <a href="https://msdn.microsoft.com/e98df845-71d9-41f9-bf05-b46014e861df">PeerGroupDelete</a> before a call to <a href="https://msdn.microsoft.com/9738f6b1-cd88-4950-bab1-f97613a49e03">PeerIdentityDelete</a> can succeed.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A peer identity that matches the specified name cannot be found.

</td>
</tr>
</table>
 



