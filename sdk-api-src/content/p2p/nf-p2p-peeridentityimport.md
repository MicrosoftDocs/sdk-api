---
UID: NF:p2p.PeerIdentityImport
title: PeerIdentityImport function (p2p.h)
author: windows-sdk-content
description: The PeerIdentityImport function imports one peer identity. If the peer identity exists on a computer, PEER_E_ALREADY_EXISTS is returned.
old-location: p2p\peeridentityimport.htm
tech.root: P2PSdk
ms.assetid: 273aa395-905a-41bd-a027-23f4b3f549b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerIdentityImport, PeerIdentityImport function [Peer Networking], p2p.peeridentityimport, p2p/PeerIdentityImport
ms.topic: function
f1_keywords: 
 - "p2p/PeerIdentityImport"
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
 - PeerIdentityImport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerIdentityImport function


## -description


The <b>PeerIdentityImport</b> function imports  one peer  identity. If the peer identity exists on a computer, <b>PEER_E_ALREADY_EXISTS</b> is returned. 


## -parameters




### -param pwzImportXML [in]

Pointer to the XML format peer identity to import, which is returned by <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peeridentityexport">PeerIdentityExport</a>. This binary data must match the exported data byte-for-byte.  The XML must remain valid XML with no extra 
characters.


### -param pwzPassword [in]

Specifies the password to use to de-crypt a peer identity. The password must be identical to the password supplied to <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peeridentityexport">PeerIdentityExport</a>. This parameter cannot be <b>NULL</b>.


### -param ppwzIdentity [out]

Pointer to a string that represents a peer identity that is imported.  If the import operation is successful, the application must free <i>ppwzIdentity</i> by calling <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>. 


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
One of the parameters is not valid, or the XML data in <i>ppwzImportXML</i> has been tampered with.

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
<dt><b>PEER_E_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The peer identity already exists on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. Typically, this is caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually.

</td>
</tr>
</table>
 




## -remarks



The XML fragment used by <b>PeerIdentityImport</b> is as follows:

<pre class="syntax" xml:space="preserve"><code>&lt;PEERIDENTITYEXPORT VERSION="1.0"&gt;
   &lt;IDENTITY&gt;
     &lt;!-- UTF-8 encoded peer name of the identity --&gt;
   &lt;/IDENTITY&gt;
   &lt;IDENTITYDATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64"&gt;
      &lt;!-- base64 encoded / PFX encoded and encrypted IDC with the private key --&gt;
   &lt;/IDENTTYDATA&gt;
&lt;/PEERIDENTITYEXPORT&gt;
</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peeridentityexport">PeerIdentityExport</a>
 

 

