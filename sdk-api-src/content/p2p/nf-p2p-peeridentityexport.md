---
UID: NF:p2p.PeerIdentityExport
title: PeerIdentityExport function (p2p.h)
description: The PeerIdentityExport function allows a user to export one peer identity. The user can then transfer the peer identity to a different computer.
helpviewer_keywords: ["PeerIdentityExport","PeerIdentityExport function [Peer Networking]","p2p.peeridentityexport","p2p/PeerIdentityExport"]
old-location: p2p\peeridentityexport.htm
tech.root: p2p
ms.assetid: 2b7cfc46-77f6-49cb-966c-0a96830c96fd
ms.date: 12/05/2018
ms.keywords: PeerIdentityExport, PeerIdentityExport function [Peer Networking], p2p.peeridentityexport, p2p/PeerIdentityExport
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerIdentityExport
 - p2p/PeerIdentityExport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerIdentityExport
---

# PeerIdentityExport function


## -description

The <b>PeerIdentityExport</b> function allows a user to export  one peer  identity. The user can then transfer the peer identity to a different computer.

## -parameters

### -param pwzIdentity [in]

Specifies the peer identity  to export. This parameter is required and does not have a default value.

### -param pwzPassword [in]

Specifies the password to use to encrypt the peer identity. This parameter cannot be <b>NULL</b>. This password must also be used to import the peer identity, or the import operation fails.

### -param ppwzExportXML [out]

Receives a pointer to the exported peer identity in XML format. If the export operation is successful, the application must free <i>ppwzExportXML</i> by calling <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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
<dt><b> PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys was denied. This is typically caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been manually reset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND </b></dt>
</dl>
</td>
<td width="60%">
The specified peer identity does not exist.

</td>
</tr>
</table>

## -remarks

Peer-to-peer group membership credentials are not exported. Only one peer identity  is  exported. An exported peer identity can be imported on another computer by using <a href="/windows/desktop/api/p2p/nf-p2p-peeridentityimport">PeerIdentityImport</a>.  

Exporting a peer identity   does not remove it from a local ccmputer, it  makes a copy of it. The copy can be used to backup and restore a peer identity. 


The XML fragment used by <b>PeerIdentityExport</b> is as follows:


``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```


## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peeridentityimport">PeerIdentityImport</a>
