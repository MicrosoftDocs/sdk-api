---
UID: NN:wdstptmgmt.IWdsTransportSession
title: IWdsTransportSession
author: windows-sdk-content
description: Represents an active transport session on the WDS transport server.
old-location: wds\iwdstransportsession.htm
old-project: wds
ms.assetid: acf417ea-2396-4178-84e5-6d6b495476f8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWdsTransportSession, IWdsTransportSession interface [Windows Deployment Services], IWdsTransportSession interface [Windows Deployment Services],described, wds.iwdstransportsession, wdstptmgmt/IWdsTransportSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportSession
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportSession interface


## -description


Represents an active transport session on the WDS transport server. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportSession</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWdsTransportSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWdsTransportSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6e41658-8d91-4c15-8a5f-a9f43490890a">RetrieveClients</a>
</td>
<td align="left" width="63%">
Retrieves a collection of WDS clients joined to the transport session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b616a69-1387-4c55-a80e-95ead719b911">Terminate</a>
</td>
<td align="left" width="63%">
Terminates an active session on the WDS transport server and disconnects all WDS clients joined to the session.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportSession</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/642026fe-976f-439f-b90d-ad9a28609f00">Content</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to an object of the <a href="https://msdn.microsoft.com/d7ed1f64-578f-4b3a-b9af-9a48800b9ca4">IWdsTransportContent</a> interface that represents an active transport session on the WDS transport server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a unique session ID that identifies this session on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6259ee20-b5ed-47c0-853a-2d3cad19b387">MasterClientId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a unique client ID assigned by the WDS server that identifies the master client for this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6585452b-037c-4ee8-807a-144b6b53695a">NetworkInterfaceAddress</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the MAC address of the server network interface used by this transport session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2408b109-6878-4c66-ba44-196c10b2ae96">NetworkInterfaceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the name of the server network interface used by this transport session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc346743-b2be-43c1-8b68-495bd0aa99d9">TransferRate</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the data transfer rate for this session in bytes per second.

</td>
</tr>
</table> 

