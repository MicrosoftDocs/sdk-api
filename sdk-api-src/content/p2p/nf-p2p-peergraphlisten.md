---
UID: NF:p2p.PeerGraphListen
title: PeerGraphListen function (p2p.h)
description: The PeerGraphListen function indicates that a peer graph should start listening for incoming connections.
helpviewer_keywords: ["PEER_GRAPH_SCOPE_GLOBAL","PEER_GRAPH_SCOPE_LINKLOCAL","PEER_GRAPH_SCOPE_SITELOCAL","PeerGraphListen","PeerGraphListen function [Peer Networking]","p2p.peergraphlisten","p2p/PeerGraphListen"]
old-location: p2p\peergraphlisten.htm
tech.root: p2p
ms.assetid: bac893d4-8f4d-4e1f-953b-1b289c5f18be
ms.date: 12/05/2018
ms.keywords: PEER_GRAPH_SCOPE_GLOBAL, PEER_GRAPH_SCOPE_LINKLOCAL, PEER_GRAPH_SCOPE_SITELOCAL, PeerGraphListen, PeerGraphListen function [Peer Networking], p2p.peergraphlisten, p2p/PeerGraphListen
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGraphListen
 - p2p/PeerGraphListen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphListen
---

# PeerGraphListen function


## -description

The <b>PeerGraphListen</b> function indicates that  a peer graph should  start listening for incoming connections.

## -parameters

### -param hGraph [in]

Specifies the peer graph to  listen  on.

### -param dwScope [in]

Specifies the IPv6 scope to listen on.  Valid values are identified in the following table. For more information about scope, see <a href="/windows/desktop/P2PSdk/graphing-reference-links">Link-Local and Site-Local Addresses</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEER_GRAPH_SCOPE_GLOBAL"></a><a id="peer_graph_scope_global"></a><dl>
<dt><b>PEER_GRAPH_SCOPE_GLOBAL</b></dt>
</dl>
</td>
<td width="60%">
Scope includes the Internet.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_GRAPH_SCOPE_SITELOCAL"></a><a id="peer_graph_scope_sitelocal"></a><dl>
<dt><b>PEER_GRAPH_SCOPE_SITELOCAL</b></dt>
</dl>
</td>
<td width="60%">
Scope is restricted to a site, for example, a corporation intranet.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_GRAPH_SCOPE_LINKLOCAL"></a><a id="peer_graph_scope_linklocal"></a><dl>
<dt><b>PEER_GRAPH_SCOPE_LINKLOCAL</b></dt>
</dl>
</td>
<td width="60%">
Scope is restricted to a local subnet.

</td>
</tr>
</table>

### -param dwScopeId [in]

Specifies the IPv6 scope ID to listen on. Specify zero (0) to listen on all interfaces of the specified scope.

<div class="alert"><b>Note</b>  The scope ID zero (0) is  not allowed if <i>dwScope</i> is <b>PEER_GRAPH_SCOPE_SITELOCAL</b> or  <b>PEER_GRAPH_SCOPE_LINKLOCAL</b>.</div>
<div> </div>

### -param wPort [in]

Specifies the port  to listen on. Specify zero (0) to use a dynamic port. If zero (0) is specified, use <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnodeinfo">PeerGraphGetNodeInfo</a> to retrieve data.

## -returns

Returns <b>S_OK</b> if the operation succeeds. Otherwise, the function returns one of the  values identified in the following table.

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
<dt><b>PEER_E_GRAPH_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The graph has never been synchronized. An application cannot listen until the peer graph has been synchronized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The graph must be initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a>—before using this function.

</td>
</tr>
</table>

## -remarks

To be able to accept direct connections, a node must  subscribe to the  <b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b> event.  

Before this function can be called, the application must  call <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>. 

<div class="alert"><b>Note</b>  If this is the first time a peer graph is opened, all calls to <b>PeerGraphListen</b>  fail until the node  connects to and synchronizes with  the peer graph.</div>
<div> </div>
The application  can specify the same port ID for different peer graphs, if all the peer graphs are in the same process.


#### Examples

The following code snippet shows how to use the <b>PeerGraphListen</b> function.


```cpp
    // g_hGraph is a handle to the Graph obtained from a previous successful call to PeerGraphCreate or PeerGraphOpen.
    // dwScope should be set to the same scope used to create the graph.  This example assumes the graph was created in the Global scope.
    // g_usPort is the port to use for Graphing.  Use zero to obtain a port dynamically.
    HRESULT hr = PeerGraphListen(g_hGraph, PEER_GRAPH_SCOPE_GLOBAL, 0, g_usPort);

    if (FAILED(hr))
    {
        // Insert your code to handle the error here.
    }
    else
    {
        // Insert your application specific code here.
    }

```

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphconnect">PeerGraphConnect</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnodeinfo">PeerGraphGetNodeInfo</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>