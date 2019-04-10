---
UID: NF:p2p.PeerIdentityGetXML
title: PeerIdentityGetXML function (p2p.h)
author: windows-sdk-content
description: The PeerIdentityGetXML function returns a description of the peer identity, which can then be passed to third parties and used to invite a peer identity into a peer group. This information is returned as an XML fragment.
old-location: p2p\peeridentitygetxml.htm
tech.root: P2PSdk
ms.assetid: 94172351-291e-461e-8c7f-0925c80df0c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerIdentityGetXML, PeerIdentityGetXML function [Peer Networking], p2p.peeridentitygetxml, p2p/PeerIdentityGetXML
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
 - PeerIdentityGetXML
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerIdentityGetXML function


## -description


The <b>PeerIdentityGetXML</b> function returns a description of the peer identity, which can then be passed to third parties and used to invite a peer identity into a peer group. This information is returned as an XML fragment.


## -parameters




### -param pwzIdentity [in]

Specifies the peer identity to retrieve peer identity information for. When this parameter is passed as <b>NULL</b>, a "default" identity will be generated for the user by the peer infrastructure.


### -param ppwzIdentityXML [out]

Pointer to a pointer to a Unicode string that contains the XML fragment. When <i>ppwzIdentityXML</i> is no longer required, the application is responsible for freeing this string by calling  <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.


## -returns



If the function call succeeds, the return value is S_OK. Otherwise, it  returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle to the  identity is invalid.

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
</table>
 




## -remarks



The XML fragment returned has the following structure:

<pre class="syntax" xml:space="preserve"><code>&lt;PEERIDENTITYINFO VERSION="1.0"&gt;
     &lt;IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64"&gt;
          Base 64 encoded certificate.
     &lt;/IDC&gt;
&lt;/PEERIDENTITYINFO&gt;</code></pre>
This XML fragment is used when creating an invitation to join a group.

Applications are not allowed to add tags within the <b>PEERIDENTITYINFO</b> tag or modify this XML fragment in any way.  Applications are allowed to incorporate this XML fragment into other XML documents, but must strip out all application-specific XML before passing this fragment to the <a href="https://msdn.microsoft.com/1ae5c288-6e9b-452a-8994-7878d713cd6d">PeerGroupCreateInvitation</a>.




## -see-also




<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>



<a href="https://msdn.microsoft.com/1ae5c288-6e9b-452a-8994-7878d713cd6d">PeerGroupCreateInvitation</a>
 

 

