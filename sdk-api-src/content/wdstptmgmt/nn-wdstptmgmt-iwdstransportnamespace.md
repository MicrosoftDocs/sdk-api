---
UID: NN:wdstptmgmt.IWdsTransportNamespace
title: IWdsTransportNamespace (wdstptmgmt.h)
description: Represents a namespace on a WDS transport server.
helpviewer_keywords: ["IWdsTransportNamespace","IWdsTransportNamespace interface [Windows Deployment Services]","IWdsTransportNamespace interface [Windows Deployment Services]","described","wds.iwdstransportnamespace","wdstptmgmt/IWdsTransportNamespace"]
old-location: wds\iwdstransportnamespace.htm
tech.root: wds
ms.assetid: eadb7b1b-aaef-4a4e-a2de-c641a4e10173
ms.date: 12/05/2018
ms.keywords: IWdsTransportNamespace, IWdsTransportNamespace interface [Windows Deployment Services], IWdsTransportNamespace interface [Windows Deployment Services],described, wds.iwdstransportnamespace, wdstptmgmt/IWdsTransportNamespace
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWdsTransportNamespace
 - wdstptmgmt/IWdsTransportNamespace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportNamespace
---

# IWdsTransportNamespace interface


## -description

Represents a namespace on a WDS transport server.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportNamespace</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportNamespace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWdsTransportNamespace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-clone">Clone</a>
</td>
<td align="left" width="63%">
Copies the information from this namespace object into a new, unregistered namespace object in memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-deregister">Deregister</a>
</td>
<td align="left" width="63%">
Deregisters the namespace on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Resets the property values of the namespace with values from the server. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-register">Register</a>
</td>
<td align="left" width="63%">
Registers the namespace on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-retrievecontents">RetrieveContents</a>
</td>
<td align="left" width="63%">
Retrieves a collection of active transport content objects associated with the namespace.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportNamespace</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_configuration">Configuration</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Receives the configuration information for the content provider of the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_contentprovider">ContentProvider</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Receives the content provider for the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Receives the description of the namespace. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_friendlyname">FriendlyName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Receives the user-friendly name of the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_id">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the unique namespace ID for a namespace that has been registered on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_name">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Receives the name of the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_tombstoned">Registered</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the namespace is registered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_tombstoned">Tombstoned</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the server has saved the namespace object of a deregistered namespace in memory until all active sessions are completed or terminated. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_tombstonetime">TombstoneTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the date and time when the server saved the namespace object of a deregistered namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_transmissionstarted">TransmissionStarted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a value that indicates whether the server has started transmitting data under this namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportnamespace-get_type">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the type of the namespace for this object.

</td>
</tr>
</table>