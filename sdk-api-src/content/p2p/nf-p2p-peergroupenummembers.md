---
UID: NF:p2p.PeerGroupEnumMembers
title: PeerGroupEnumMembers function
author: windows-sdk-content
description: The PeerGroupEnumMembers function creates an enumeration of available peer group members and the associated membership information.
old-location: p2p\peergroupenummembers.htm
old-project: P2PSdk
ms.assetid: 1201ce0b-961a-4848-9b9c-ad6491e3ff4a
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: PEER_MEMBER_PRESENT, PeerGroupEnumMembers, PeerGroupEnumMembers function [Peer Networking], p2p.peergroupenummembers, p2p/PeerGroupEnumMembers
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerGroupEnumMembers
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGroupEnumMembers function


## -description



      The <b>PeerGroupEnumMembers</b> function creates an enumeration of available peer group members and the associated membership information.


## -parameters




### -param hGroup [in]

Handle to the peer group whose members are enumerated. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param dwFlags [in]

Specifies the <a href="https://msdn.microsoft.com/96a8e4ae-dce6-4f07-ab22-71da347ef347">PEER_MEMBER_FLAGS</a> flags that indicate which types of members to include in the enumeration. If this value is set to zero, all members of the peer group are included.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEER_MEMBER_PRESENT"></a><a id="peer_member_present"></a><dl>
<dt><b>PEER_MEMBER_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all members of the current peer group that are online.

</td>
</tr>
</table>
 


### -param pwzIdentity [in]

Unicode string that contains the identity of a specific peer whose information is  retrieved and returned in a one-item enumeration. If this parameter is <b>NULL</b>, all members of the current peer group are retrieved. This parameter is required.


### -param phPeerEnum [out]

Pointer to the enumeration that contains the returned list of peer group members. This handle is passed to  
	 <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a> to retrieve the items, with each item represented as a pointer to a <a href="https://msdn.microsoft.com/b8bd0e17-6af7-426d-ba38-11ff4948cf67">PEER_MEMBER</a> structure. When finished, <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a> is called to return the memory used by the enumeration. This parameter is required.


## -returns



Returns S_OK  if the operation succeeds. Otherwise, the function returns one of the following values.

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
<dt><b>PEER_E_INVALID_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer group is invalid.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



The local node is always the very first item in the enumeration if <i>pwzIdentity</i> is <b>NULL</b>, and <i>dwFlags</i> is set to indicate that the local node is a member of the explicit subset.

By default, every member publishes membership information to the peer group. If <a href="https://msdn.microsoft.com/ce8a4245-391d-4433-8811-8d190d94815c">PEER_MEMBER_DATA_OPTIONAL</a> is set on the <a href="https://msdn.microsoft.com/b8bd0e17-6af7-426d-ba38-11ff4948cf67">PEER_MEMBER</a> data for that peer, this information is only  available when a peer performs an action within the group, for example, publishing a record, updating presence, or issuing a GMC.




## -see-also




<a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>



<a href="https://msdn.microsoft.com/8f6fec31-8867-4d65-b5b0-e6506be9c991">PeerGetItemCount</a>



<a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>
 

 

