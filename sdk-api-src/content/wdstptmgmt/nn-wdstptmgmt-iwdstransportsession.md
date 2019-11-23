---
UID: NN:wdstptmgmt.IWdsTransportSession
title: IWdsTransportSession (wdstptmgmt.h)

description: Represents an active transport session on the WDS transport server.
old-location: wds\iwdstransportsession.htm
tech.root: wds
ms.assetid: acf417ea-2396-4178-84e5-6d6b495476f8

ms.date: 12/05/2018
ms.keywords: IWdsTransportSession, IWdsTransportSession interface [Windows Deployment Services], IWdsTransportSession interface [Windows Deployment Services],described, wds.iwdstransportsession, wdstptmgmt/IWdsTransportSession
ms.topic: interface
f1_keywords: 
 - "wdstptmgmt/IWdsTransportSession"
dev_langs:
 - c++
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
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportSession interface


## -description


Represents an active transport session on the WDS transport server. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportSession</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportSession</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsession-retrieveclients">RetrieveClients</a>
</td>
<td align="left" width="63%">
Retrieves a collection of WDS clients joined to the transport session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsession-terminate">Terminate</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsession-get_content">Content</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to an object of the <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcontent">IWdsTransportContent</a> interface that represents an active transport session on the WDS transport server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsession-get_id">Id</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsession-get_masterclientid">MasterClientId</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsession-get_networkinterfaceaddress">NetworkInterfaceAddress</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsession-get_networkinterfacename">NetworkInterfaceName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsession-get_transferrate">TransferRate</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the data transfer rate for this session in bytes per second.

</td>
</tr>
</table> 

