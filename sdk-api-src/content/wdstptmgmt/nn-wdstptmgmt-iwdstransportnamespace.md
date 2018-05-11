---
UID: NN:wdstptmgmt.IWdsTransportNamespace
title: IWdsTransportNamespace
author: windows-driver-content
description: Represents a namespace on a WDS transport server.
old-location: wds\iwdstransportnamespace.htm
old-project: Wds
ms.assetid: eadb7b1b-aaef-4a4e-a2de-c641a4e10173
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWdsTransportNamespace, IWdsTransportNamespace interface [Windows Deployment Services], IWdsTransportNamespace interface [Windows Deployment Services],described, wds.iwdstransportnamespace, wdstptmgmt/IWdsTransportNamespace
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wdstptmgmt.dll
api_name:
-	IWdsTransportNamespace
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportNamespace interface


## -description


Represents a namespace on a WDS transport server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportNamespace</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWdsTransportNamespace</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Copies the information from this namespace object into a new, unregistered namespace object in memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32881121-b5aa-4ccf-9884-431dbd283e4c">Deregister</a>
</td>
<td align="left" width="63%">
Deregisters the namespace on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d5742e0-4197-4a15-82c6-5623940c0c7f">Refresh</a>
</td>
<td align="left" width="63%">
Resets the property values of the namespace with values from the server. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b5d2bf7-c06b-4e1b-bb98-e17a9816c90f">Register</a>
</td>
<td align="left" width="63%">
Registers the namespace on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78afaf1c-f29f-4ab0-8329-d2199ea49c43">RetrieveContents</a>
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

<a href="https://msdn.microsoft.com/library/windows/hardware/ff539567">Configuration</a>


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

<a href="https://msdn.microsoft.com/9c37f1d2-fd56-43c1-8565-bc60fc6894de">ContentProvider</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


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

<a href="https://msdn.microsoft.com/09964bb7-fddb-48e2-891a-d1f2fd8763eb">FriendlyName</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn965826">Registered</a>


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

<a href="https://msdn.microsoft.com/a04b578b-ad18-46b0-a60e-77647fa67aaf">Tombstoned</a>


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

<a href="https://msdn.microsoft.com/95516e2b-40e3-4da8-9ca0-0f96a8e6cb13">TombstoneTime</a>


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

<a href="https://msdn.microsoft.com/abc395e5-aabe-478b-8232-48a107813da9">TransmissionStarted</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the type of the namespace for this object.

</td>
</tr>
</table> 

