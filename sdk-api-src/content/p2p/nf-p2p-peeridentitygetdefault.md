---
UID: NF:p2p.PeerIdentityGetDefault
title: PeerIdentityGetDefault function
author: windows-sdk-content
description: The PeerIdentityGetDefault function retrieves the default peer name set for the current user.
old-location: p2p\peeridentitygetdefault.htm
tech.root: P2PSdk
ms.assetid: 195052a2-eaae-4b8c-bc13-0667ce50a967
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PeerIdentityGetDefault, PeerIdentityGetDefault function [Peer Networking], p2p.peeridentitygetdefault, p2p/PeerIdentityGetDefault
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PeerIdentityGetDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerIdentityGetDefault function


## -description


The <b>PeerIdentityGetDefault</b> function retrieves the default peer name set for the current user.


## -parameters




### -param ppwzPeerName [out]

Pointer to the address of a zero-terminated Unicode string that contains the default name of the current user.


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
There is not enough memory to perform the specified operation.

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
 



