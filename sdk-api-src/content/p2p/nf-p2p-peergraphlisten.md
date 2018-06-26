---
UID: NF:p2p.PeerGraphListen
title: PeerGraphListen function
author: windows-sdk-content
description: The PeerGraphListen function indicates that a peer graph should start listening for incoming connections.
old-location: p2p\peergraphlisten.htm
old-project: P2PSdk
ms.assetid: bac893d4-8f4d-4e1f-953b-1b289c5f18be
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PEER_GRAPH_SCOPE_GLOBAL, PEER_GRAPH_SCOPE_LINKLOCAL, PEER_GRAPH_SCOPE_SITELOCAL, PeerGraphListen, PeerGraphListen function [Peer Networking], p2p.peergraphlisten, p2p/PeerGraphListen
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
 - P2PGraph.dll
api_name:
 - PeerGraphListen
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: ADAM
---

# PeerGraphListen function


## -description



      The <b>PeerGraphListen</b> function indicates that  a peer graph should  start listening for incoming connections.

## -parameters




### -param hGraph [in]

Specifies the peer graph to  listen  on.


### -param dwScope [in]

Specifies the IPv6 scope to listen on.  Valid values are identified in the following table. For more information about scope, see <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">Link-Local and Site-Local Addresses</a>.

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

Specifies the port  to listen on. Specify zero (0) to use a dynamic port. If zero (0) is specified, use <a href="https://msdn.microsoft.com/7149aba3-d44b-4492-aa56-4d8dbfba7b7c">PeerGraphGetNodeInfo</a> to retrieve data.


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
The graph must be initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a>—before using this function.

</td>
</tr>
</table>
 




## -remarks



To be able to accept direct connections, a node must  subscribe to the  <b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b> event.  


        Before this function can be called, the application must  call <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a> or <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>. 

<div class="alert"><b>Note</b>  If this is the first time a peer graph is opened, all calls to <b>PeerGraphListen</b>  fail until the node  connects to and synchronizes with  the peer graph.</div>
<div> </div>
The application  can specify the same port ID for different peer graphs, if all the peer graphs are in the same process.


#### Examples

The following code snippet shows how to use the <b>PeerGraphListen</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    // g_hGraph is a handle to the Graph obtained from a previous successful call to PeerGraphCreate or PeerGraphOpen.
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/76a2c54d-4424-4aa3-9b62-3ebe88b63c9f">PeerGraphConnect</a>



<a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>



<a href="https://msdn.microsoft.com/7149aba3-d44b-4492-aa56-4d8dbfba7b7c">PeerGraphGetNodeInfo</a>



<a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>
 

 

