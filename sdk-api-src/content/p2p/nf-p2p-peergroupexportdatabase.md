---
UID: NF:p2p.PeerGroupExportDatabase
title: PeerGroupExportDatabase function
author: windows-sdk-content
description: The PeerGroupExportDatabase function exports a peer group database to a specific file, which can be transported to another computer and imported with the PeerGroupImportDatabase function.
old-location: p2p\peergroupexportdatabase.htm
old-project: P2PSdk
ms.assetid: ce448780-5a9b-4d2d-9dfb-192b4e6c1b22
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerGroupExportDatabase, PeerGroupExportDatabase function [Peer Networking], p2p.peergroupexportdatabase, p2p/PeerGroupExportDatabase
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
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerGroupExportDatabase
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGroupExportDatabase function


## -description



      The <b>PeerGroupExportDatabase</b> function exports a peer  group database to a specific file, which can be transported to another computer and imported with the <a href="https://msdn.microsoft.com/507b2b51-07d1-4e8d-8ec6-6b7398eadcc0">PeerGroupImportDatabase</a> function.


## -parameters




### -param hGroup [in]

Handle to the peer group whose database is exported to a local file on the peer. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


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
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/507b2b51-07d1-4e8d-8ec6-6b7398eadcc0">PeerGroupImportDatabase</a>
 

 

