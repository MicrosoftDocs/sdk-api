---
UID: NN:sbtsv.ITsSbClientConnection
title: ITsSbClientConnection
author: windows-sdk-content
description: Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.
old-location: termserv\itssbclientconnection.htm
tech.root: TermServ
ms.assetid: 6649f43d-0e2a-42d7-8111-862bb28e3dbc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITsSbClientConnection, ITsSbClientConnection interface [Remote Desktop Services], ITsSbClientConnection interface [Remote Desktop Services],described, sbtsv/ITsSbClientConnection, termserv.itssbclientconnection
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbClientConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbClientConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbClientConnection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/dd4938b5-aa33-4eca-851c-fdef75ecc815">GetContext</a>
</td>
<td align="left" width="63%">
Retrieves context information that was stored by a plug-in by using the 
       <a href="https://msdn.microsoft.com/654714ef-cc86-41e8-8759-bbb66bd61cd2">PutContext</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fb6d2af-a60c-4173-a2c0-9d9ce5d26811">GetDisconnectedSession</a>
</td>
<td align="left" width="63%">
Gets a disconnected session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/654714ef-cc86-41e8-8759-bbb66bd61cd2">PutContext</a>
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

<a href="https://msdn.microsoft.com/488c5b71-7139-4744-93bf-484d05457d0f">ClientConnectionPropertySet</a>


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

<a href="https://msdn.microsoft.com/0aa813c1-1ab5-4020-8180-c04d293efd25">ConnectionError</a>


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

<a href="https://msdn.microsoft.com/628f450d-10f4-4405-8d7c-ae58c72c2755">Domain</a>


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

<a href="https://msdn.microsoft.com/97fe4851-96a9-4b23-8ad7-f42b87c655d0">Environment</a>


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

<a href="https://msdn.microsoft.com/8734b130-f1fd-4107-b0cc-482b78647ac7">InitialProgram</a>


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

<a href="https://msdn.microsoft.com/fdcd094c-d50b-4cdd-8164-23c24bb7017b">LoadBalanceResult</a>


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

<a href="https://msdn.microsoft.com/eb3d8e6b-60c6-4d24-824c-94b642f44956">SamUserAccount</a>


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

<a href="https://msdn.microsoft.com/74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54">UserName</a>


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




<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

