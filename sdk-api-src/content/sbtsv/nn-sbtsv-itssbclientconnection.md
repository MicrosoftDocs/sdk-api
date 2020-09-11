---
UID: NN:sbtsv.ITsSbClientConnection
title: ITsSbClientConnection (sbtsv.h)
description: Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.
helpviewer_keywords: ["ITsSbClientConnection","ITsSbClientConnection interface [Remote Desktop Services]","ITsSbClientConnection interface [Remote Desktop Services]","described","sbtsv/ITsSbClientConnection","termserv.itssbclientconnection"]
old-location: termserv\itssbclientconnection.htm
tech.root: TermServ
ms.assetid: 6649f43d-0e2a-42d7-8111-862bb28e3dbc
ms.date: 12/05/2018
ms.keywords: ITsSbClientConnection, ITsSbClientConnection interface [Remote Desktop Services], ITsSbClientConnection interface [Remote Desktop Services],described, sbtsv/ITsSbClientConnection, termserv.itssbclientconnection
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbClientConnection
 - sbtsv/ITsSbClientConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbClientConnection
---

# ITsSbClientConnection interface


## -description

Exposes methods and properties that store state information about an incoming connection request from a 
    Remote Desktop  Connection (RDC) client. This information does not need to be stored on the resource or 
    filter plug-ins, which allows the plug-ins to be stateless.

Plug-ins can use this interface to obtain information about a connection request initiated by a client, and then 
    make decisions about load balancing, placement, and orchestration. This interface also stores the results of all 
    these operations. A <b>ITsSbClientConnection</b> object 
    should persist until the client successfully logs on to a target computer.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbClientConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbClientConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITsSbClientConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Retrieves context information that was stored by a plug-in by using the 
       <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-putcontext">PutContext</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-getdisconnectedsession">GetDisconnectedSession</a>
</td>
<td align="left" width="63%">
Gets a disconnected session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-putcontext">PutContext</a>
</td>
<td align="left" width="63%">
Can be used by plug-ins to store context information specific to the connection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbClientConnection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-get_clientconnectionpropertyset">ClientConnectionPropertySet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The property set object for this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-get_connectionerror">ConnectionError</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The error that occurred while a client connection was being processed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/TermServ/itssbclientconnection-domain">Domain</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The domain name of the Remote Desktop Connection (RDC) client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/TermServ/itssbclientconnection-environment">Environment</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The environment that hosts the target computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-get_initialprogram">InitialProgram</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The program that is launched when the user logs on to the target computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-get_loadbalanceresult">LoadBalanceResult</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the target computer returned by load balancing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbclientconnection-get_samuseraccount">SamUserAccount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The domain name and user name of the user who initiated the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/TermServ/itssbclientconnection-username">UserName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the user who initiated the connection.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>

