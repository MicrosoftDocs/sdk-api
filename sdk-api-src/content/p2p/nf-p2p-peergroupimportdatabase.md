---
UID: NF:p2p.PeerGroupImportDatabase
title: PeerGroupImportDatabase function
author: windows-driver-content
description: The PeerGroupImportDatabase function imports a peer group database from a local file.
old-location: p2p\peergroupimportdatabase.htm
old-project: P2PSdk
ms.assetid: 507b2b51-07d1-4e8d-8ec6-6b7398eadcc0
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerGroupImportDatabase, PeerGroupImportDatabase function [Peer Networking], p2p.peergroupimportdatabase, p2p/PeerGroupImportDatabase
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
-	PeerGroupImportDatabase
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGroupImportDatabase function


## -description



      The <b>PeerGroupImportDatabase</b> function imports a peer group database from a local file.


## -parameters




### -param hGroup [in]

Handle to a peer group whose database is imported from a local file. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param pwzFilePath [in]

Pointer to a Unicode string that contains the absolute file system path and file name where the data is stored, for example, "C:\backup\p2pdb.db". If the file does not exist at this location, an appropriate error from the file system is returned. This parameter is required.


## -returns



Returns <b>S_OK</b>  if the operation succeeds. Otherwise, the function returns one of the following values.

<div class="alert"><b>Note</b>  If an import fails due to a file system error, the appropriate file system error is returned.</div>
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
<dt><b>PEER_E_GROUP_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be completed because the peer group database is currently in use. For example, <a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a> has been called by a peer, but has not yet completed any database transactions.

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



This function must be called before <a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a>, and after <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a> or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>. 




## -see-also




<a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/ce448780-5a9b-4d2d-9dfb-192b4e6c1b22">PerrGroupExportDatabase</a>
 

 

