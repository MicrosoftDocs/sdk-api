---
UID: NF:p2p.PeerGroupExportDatabase
title: PeerGroupExportDatabase function (p2p.h)
description: The PeerGroupExportDatabase function exports a peer group database to a specific file, which can be transported to another computer and imported with the PeerGroupImportDatabase function.
helpviewer_keywords: ["PeerGroupExportDatabase","PeerGroupExportDatabase function [Peer Networking]","p2p.peergroupexportdatabase","p2p/PeerGroupExportDatabase"]
old-location: p2p\peergroupexportdatabase.htm
tech.root: p2p
ms.assetid: ce448780-5a9b-4d2d-9dfb-192b4e6c1b22
ms.date: 12/05/2018
ms.keywords: PeerGroupExportDatabase, PeerGroupExportDatabase function [Peer Networking], p2p.peergroupexportdatabase, p2p/PeerGroupExportDatabase
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
 - PeerGroupExportDatabase
 - p2p/PeerGroupExportDatabase
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
 - PeerGroupExportDatabase
---

# PeerGroupExportDatabase function


## -description

The <b>PeerGroupExportDatabase</b> function exports a peer  group database to a specific file, which can be transported to another computer and imported with the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupimportdatabase">PeerGroupImportDatabase</a> function.

## -parameters

### -param hGroup [in]

Handle to the peer group whose database is exported to a local file on the peer. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pwzFilePath [in]

Pointer to a Unicode string that contains the absolute file system path and file name where the exported database is stored. For example, "C:\backup\p2pdb.db". If this file already exists at the specified location, the older file is overwritten. This parameter is required.

## -returns

Returns S_OK  if the operation succeeds. Otherwise, the function returns one of the following values.

<div class="alert"><b>Note</b>  If an export fails due to a file system error, the appropriate file system error, defined in winerror.h, is returned.</div>
<div> </div>
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
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupimportdatabase">PeerGroupImportDatabase</a>