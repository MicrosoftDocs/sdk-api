---
UID: NF:p2p.PeerGraphEndEnumeration
title: PeerGraphEndEnumeration function (p2p.h)
author: windows-sdk-content
description: The PeerGraphEndEnumeration function releases an enumeration handle, and frees the resources associated with an enumeration.
old-location: p2p\peergraphendenumeration.htm
tech.root: P2PSdk
ms.assetid: 31a18705-b8bf-461c-98e0-c03c6d269b51
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGraphEndEnumeration, PeerGraphEndEnumeration function [Peer Networking], p2p.peergraphendenumeration, p2p/PeerGraphEndEnumeration
ms.topic: function
f1_keywords: 
 - "p2p/PeerGraphEndEnumeration"
dev_langs:
 - c++
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
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphEndEnumeration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerGraphEndEnumeration function


## -description


The <b>PeerGraphEndEnumeration</b> function releases an enumeration handle,  and frees the resources associated with an enumeration.


## -parameters




### -param hPeerEnum [in]

Handle to an  enumeration to release. This handle is  returned by one of the following functions: <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphenumconnections">PeerGraphEnumConnections</a>, <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphenumnodes">PeerGraphEnumNodes</a>, <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphenumrecords">PeerGraphEnumRecords</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphsearchrecords">PeerGraphSearchRecords</a>.


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
A parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
A graph must be  initialized with a call to <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphenumconnections">PeerGraphEnumConnections</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphenumnodes">PeerGraphEnumNodes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphenumrecords">PeerGraphEnumRecords</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphsearchrecords">PeerGraphSearchRecords</a>
 

 

