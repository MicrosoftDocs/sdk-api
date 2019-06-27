---
UID: NF:p2p.PeerCollabShutdown
title: PeerCollabShutdown function (p2p.h)
author: windows-sdk-content
description: Shuts down the Peer Collaboration infrastructure and releases any resources associated with it.
old-location: p2p\peercollabshutdown.htm
tech.root: P2PSdk
ms.assetid: 4e328188-c8a1-4ba9-817b-3d130a64b985
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerCollabShutdown, PeerCollabShutdown function [Peer Networking], p2p.peercollabshutdown, p2p/PeerCollabShutdown
ms.topic: function
f1_keywords: 
 - "p2p/PeerCollabShutdown"
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - PeerCollabShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerCollabShutdown function


## -description


The <b>PeerCollabShutdown</b> function shuts down the Peer Collaboration infrastructure and releases any resources associated with it.


## -parameters






## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The application did not make a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peercollabstartup">PeerCollabStartup</a>.

</td>
</tr>
</table>
 




## -remarks



A call to this function decreases the number of references to the Peer Collaboration infrastructure by 1. If the reference count equals 0, then all resources associated with the Peer Collaboration infrastructure are released.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peercollabstartup">PeerCollabStartup</a>
 

 

