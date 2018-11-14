---
UID: NN:faxcomex.IFaxOutboundRoutingGroups
title: IFaxOutboundRoutingGroups
author: windows-sdk-content
description: The IFaxOutboundRoutingGroups interface describes a configuration collection used by a fax client application to manage the fax outbound routing groups, represented by IFaxOutboundRoutingGroup interfaces.
old-location: fax\_mfax_faxoutboundroutinggroups_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_62r7_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutboundRoutingGroups, IFaxOutboundRoutingGroups interface [Fax Service], IFaxOutboundRoutingGroups interface [Fax Service],described, _mfax_faxoutboundroutinggroups_cpp, fax._mfax_faxoutboundroutinggroups_cpp, faxcomex/IFaxOutboundRoutingGroups
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutboundRoutingGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingGroups interface


## -description


The <b>IFaxOutboundRoutingGroups</b> interface describes a configuration collection used by a fax client application to manage the fax outbound routing groups, represented by <a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a> interfaces. The interface also includes methods to add and remove groups from the collection.
<div class="alert"><b>Note</b>  The outbound routing group <b>All Devices</b> is always the first object in this collection. You cannot remove the <b>All Devices</b> group from the collection. If you attempt to remove it, you will receive an error message.
</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRoutingGroups</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutboundRoutingGroups</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutboundRoutingGroups</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82278aba-aa52-4a22-84f6-dadcd7e94376">Add</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/82278aba-aa52-4a22-84f6-dadcd7e94376">IFaxOutboundRoutingGroups::Add</a> method adds an outbound routing group to the collection represented by the <b>IFaxOutboundRoutingGroups</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/900641f5-bd73-438d-b156-947a97a64173">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/900641f5-bd73-438d-b156-947a97a64173">IFaxOutboundRoutingGroups::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/799a034c-c807-428c-8536-bc68dce5cd8e">FaxOutboundRoutingGroups</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f6a2110-885b-46ef-9914-389463c45845">Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1f6a2110-885b-46ef-9914-389463c45845">IFaxOutboundRoutingGroups::get_Item</a> method returns a <a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a> interface from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94958169-332f-4d9f-ac16-d35d38fd5a27">Remove</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/94958169-332f-4d9f-ac16-d35d38fd5a27">Remove</a> method removes an item from the <a href="https://msdn.microsoft.com/799a034c-c807-428c-8536-bc68dce5cd8e">FaxOutboundRoutingGroups</a> collection. 

<div class="alert"><b>Note</b>  You cannot remove the special <b>All Devices</b> routing group.</div>
<div> </div>
</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRoutingGroups</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7868b224-29e4-4306-847a-dcbda82fcde2">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7868b224-29e4-4306-847a-dcbda82fcde2">Count</a> property represents the number of objects in the <a href="https://msdn.microsoft.com/799a034c-c807-428c-8536-bc68dce5cd8e">FaxOutboundRoutingGroups</a> collection. This is the total number of outbound routing groups associated with the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutboundRoutingGroups</b> is provided as the <a href="https://msdn.microsoft.com/799a034c-c807-428c-8536-bc68dce5cd8e">FaxOutboundRoutingGroups</a> object.



