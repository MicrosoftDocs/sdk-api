---
UID: NF:p2p.PeerGroupGetProperties
title: PeerGroupGetProperties function (p2p.h)
author: windows-sdk-content
description: The PeerGroupGetProperties function retrieves information on the properties of a specified group.
old-location: p2p\peergroupgetproperties.htm
tech.root: P2PSdk
ms.assetid: 6273817f-9698-4c0b-93a9-9bbee2e5dc78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerGroupGetProperties, PeerGroupGetProperties function [Peer Networking], p2p.peergroupgetproperties, p2p/PeerGroupGetProperties
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
 - PeerGroupGetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGroupGetProperties function


## -description


The <b>PeerGroupGetProperties</b> function retrieves information on the properties of a specified group.


## -parameters




### -param hGroup [in]

Handle to a peer group whose properties are retrieved. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param ppProperties [out]

Pointer to a  <a href="https://msdn.microsoft.com/a1501343-bd84-4dbe-91d0-c64c59e34abc">PEER_GROUP_PROPERTIES</a> structure that contains information about peer   group properties. This data must be freed with <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>. This parameter is required.


## -returns



Returns <b>S_OK</b>  if the operation succeeds. Otherwise, the function returns one of the following values.

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
<dt><b>PEER_E_GROUP_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The group is not in a state where peer group properties can be retrieved. For example, <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>  is called, but synchronization with the group database has not completed.

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



Group properties cannot be retrieved if a peer has not synchronized with a peer group database. To synchronize with a peer group database before calling this function, first call <a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a>.




## -see-also




<a href="https://msdn.microsoft.com/a1501343-bd84-4dbe-91d0-c64c59e34abc">PEER_GROUP_PROPERTIES</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/20acf963-de8f-4bcd-a9d6-a513d516b108">PeerGroupSetProperties</a>
 

 

