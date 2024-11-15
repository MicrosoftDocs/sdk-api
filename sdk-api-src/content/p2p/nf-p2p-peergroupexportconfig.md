---
UID: NF:p2p.PeerGroupExportConfig
title: PeerGroupExportConfig function (p2p.h)
description: The PeerGroupExportConfig function exports the group configuration for a peer as an XML string that contains the identity, group name, and the GMC for the identity.
helpviewer_keywords: ["PeerGroupExportConfig","PeerGroupExportConfig function [Peer Networking]","p2p.peergroupexportconfig","p2p/PeerGroupExportConfig"]
old-location: p2p\peergroupexportconfig.htm
tech.root: p2p
ms.assetid: 95fe1336-4bf2-4a4b-a451-90f2ae2639c2
ms.date: 12/05/2018
ms.keywords: PeerGroupExportConfig, PeerGroupExportConfig function [Peer Networking], p2p.peergroupexportconfig, p2p/PeerGroupExportConfig
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGroupExportConfig
 - p2p/PeerGroupExportConfig
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
 - PeerGroupExportConfig
---

# PeerGroupExportConfig function


## -description

The <b>PeerGroupExportConfig</b> function exports the group configuration for a peer as an XML string that contains the identity, group name, and the  GMC for the identity.

## -parameters

### -param hGroup [in]

Handle to the group. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pwzPassword [in]

Specifies the password used to protect the exported configuration. There are no rules or limits for the formation of this password. This parameter is required.

### -param ppwzXML [out]

Pointer to the returned XML configuration string that contains the identity, group peer name, cloud peer name, group scope, and the GMC for the identity. This parameter is required.

## -returns

Returns <b>S_OK</b> if the function succeeds. Otherwise, the function returns one of the following values.

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
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the identity or group keys is denied. Typically, this is caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL is reset  manually . 


</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft Base Cryptographic Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

After being exported, this configuration can be passed out-of-band to another peer, where the configuration of the identity can be established. To import the configuration, pass  the XML string returned by this function with the password set on it to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupimportconfig">PeerGroupImportConfig</a>.

The configuration XML string appears in the following format:


``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD containing cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

