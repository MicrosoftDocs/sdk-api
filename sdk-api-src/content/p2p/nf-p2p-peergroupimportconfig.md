---
UID: NF:p2p.PeerGroupImportConfig
title: PeerGroupImportConfig function (p2p.h)
description: The PeerGroupImportConfig function imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.
helpviewer_keywords: ["PeerGroupImportConfig","PeerGroupImportConfig function [Peer Networking]","p2p.peergroupimportconfig","p2p/PeerGroupImportConfig"]
old-location: p2p\peergroupimportconfig.htm
tech.root: p2p
ms.assetid: e459f2f9-b118-4e22-8b32-65d389795664
ms.date: 12/05/2018
ms.keywords: PeerGroupImportConfig, PeerGroupImportConfig function [Peer Networking], p2p.peergroupimportconfig, p2p/PeerGroupImportConfig
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
 - PeerGroupImportConfig
 - p2p/PeerGroupImportConfig
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
 - PeerGroupImportConfig
---

# PeerGroupImportConfig function


## -description

The <b>PeerGroupImportConfig</b> function imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.

## -parameters

### -param pwzXML [in]

Specifies a Unicode string that contains a previously exported (using <a href="/windows/desktop/api/p2p/nf-p2p-peergroupexportconfig">PeerGroupExportConfig</a>) peer group configuration. For the specific XML format of the  string, see to the Remarks section of this topic. This parameter is required.

### -param pwzPassword [in]

Specifies the password used to access  the encrypted peer group configuration data, as a Unicode string. This parameter is required.

### -param fOverwrite [in]

If true, the existing group configuration is overwritten. If false, the group configuration is written only if a previous group configuration does not exist. The default value is false. This parameter is required.

### -param ppwzIdentity [out]

Contains the peer identity returned after an import completes. This parameter is required.

### -param ppwzGroup [out]

Contains a peer group peer name returned after an import completes. This parameter is required.

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
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A peer group configuration already exists, and <i>fOverwrite</i> is set to false.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

To generate a peer group configuration, call <a href="/windows/desktop/api/p2p/nf-p2p-peergroupexportconfig">PeerGroupExportConfig</a>, pass in an identity to export,  a password, and a handle to the peer group.

The configuration XML string appears in the following format:


``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the peer group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

