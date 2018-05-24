---
UID: NF:p2p.PeerIdentityCreate
title: PeerIdentityCreate function
author: windows-driver-content
description: The PeerIdentityCreate function creates a new peer identity and returns its name.
old-location: p2p\peeridentitycreate.htm
old-project: P2PSdk
ms.assetid: 24600215-afa0-4e6b-8455-b19b0de60b65
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerIdentityCreate, PeerIdentityCreate function [Peer Networking], p2p.peeridentitycreate, p2p/PeerIdentityCreate
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerIdentityCreate
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerIdentityCreate function


## -description



      The <b>PeerIdentityCreate</b> function creates a new peer identity and returns its name.  The name of the peer identity must be passed in all subsequent calls to the Peer Identity Manager, Peer Grouping, or PNRP functions that operate on behalf of the peer identity. The peer identity name specifies which peer identity is being used.


## -parameters




### -param pwzClassifier [in]

Specifies the classifier to append to the published peer identity name. This string is a Unicode string, and can be <b>NULL</b>. This string can only be 150 characters long, including the  <b>NULL</b> terminator.


### -param pwzFriendlyName [in]

Specifies the friendly name of the peer identity. This  is a Unicode string, and can be <b>NULL</b>. This string can only be 256 characters long, including the  <b>NULL</b> terminator. If <i>pwzFriendlyName</i> is <b>NULL</b>, the name of the identity is the friendly name.  The friendly name is optional, and it does not have to be unique.


### -param hCryptProv [in]

Handle to the cryptographic service provider (CSP) that contains an AT_KEYEXCHANGE key pair of at least 1024 bits in length. This key pair is used as the basis for a new peer identity. If <i>hCryptProv</i> is zero (0), a new key pair is generated for the peer identity. 

<div class="alert"><b>Note</b>  The Identity Manager API does not support a CSP that has user protected keys. If  a CSP that has user protected keys  is used, <b>PeerIdentityCreate</b> returns <b>E_INVALIDARG</b>. </div>
<div> </div>

### -param ppwzIdentity [out]

Receives a pointer to the name of an peer identity that is created. This name must be used in all subsequent calls to  the Peer Identity Manager, Peer Grouping, or PNRP functions that operate on behalf of the peer identity. Returns <b>NULL</b> if the peer identity cannot be created.


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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle to the key specified by <i>hCryptProv</i> is not valid.

</td>
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
<dt><b>PEER_E_ALREADY_EXISTS
</b></dt>
</dl>
</td>
<td width="60%">
The peer identity already exists. Only occurs if an peer identity  based on the specified key and classifier already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. Typically, this is caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_TOO_MANY_IDENTITIES</b></dt>
</dl>
</td>
<td width="60%">
The peer identity cannot be created because there are too many peer identities.

</td>
</tr>
</table>
 




## -remarks



The key pair and the classifier are used to generate the peer name of a new peer identity.  After an peer identity is created, it is automatically stored on the disk.

The name of the identity should be freed by using <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.  This does not delete the peer identity.  To delete the identity, use <a href="https://msdn.microsoft.com/9738f6b1-cd88-4950-bab1-f97613a49e03">PeerIdentityDelete</a> function.

If <i>hCryptProv</i> is not <b>NULL</b>, it can be released by using <a href="https://msdn.microsoft.com/fbd7043d-b2b5-4183-8528-01d3892053e8">CryptReleaseContext</a> after the call returns.




## -see-also




<a href="https://msdn.microsoft.com/fbd7043d-b2b5-4183-8528-01d3892053e8">CryptReleaseContext</a>



<a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>



<a href="https://msdn.microsoft.com/9738f6b1-cd88-4950-bab1-f97613a49e03">PeerIdentityDelete</a>
 

 

