---
UID: NF:p2p.PeerGroupParseInvitation
title: PeerGroupParseInvitation function
author: windows-driver-content
description: The PeerGroupParseInvitation function returns a PEER_INVITATION_INFO structure with the details of a specific invitation.
old-location: p2p\peergroupparseinvitation.htm
old-project: P2PSdk
ms.assetid: ddc1c419-7be3-4115-af21-1108921c7b1d
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerGroupParseInvitation, PeerGroupParseInvitation function [Peer Networking], p2p.peergroupparseinvitation, p2p/PeerGroupParseInvitation
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
-	PeerGroupParseInvitation
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerGroupParseInvitation function


## -description



      The <b>PeerGroupParseInvitation</b> function returns a <a href="https://msdn.microsoft.com/215df4ed-83e3-40c3-a38e-89d92ce38707">PEER_INVITATION_INFO</a> structure with the details of a specific invitation.


## -parameters




### -param pwzInvitation [in]

Pointer to a Unicode string that contains the specific peer group invitation. This parameter is required.


### -param ppInvitationInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/215df4ed-83e3-40c3-a38e-89d92ce38707">PEER_INVITATION_INFO</a> structure with the details of a specific invitation. To release the resources used by this structure, pass this pointer to  <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>. This parameter is required.


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
There is not enough memory available to complete an operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVITATION_NOT_TRUSTED</b></dt>
</dl>
</td>
<td width="60%">
The invitation is not trusted by the peer. It has been altered or contains errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_UNSUPPORTED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The invitation is not supported by the current version of the Peer Infrastructure.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/215df4ed-83e3-40c3-a38e-89d92ce38707">
		  PEER_INVITATION_INFO</a>



<a href="https://msdn.microsoft.com/1ae5c288-6e9b-452a-8994-7878d713cd6d">PeerGroupCreateInvitation</a>
 

 

