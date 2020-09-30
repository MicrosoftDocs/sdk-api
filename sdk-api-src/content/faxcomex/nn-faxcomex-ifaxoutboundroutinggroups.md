---
UID: NN:faxcomex.IFaxOutboundRoutingGroups
title: IFaxOutboundRoutingGroups (faxcomex.h)
description: The IFaxOutboundRoutingGroups interface describes a configuration collection used by a fax client application to manage the fax outbound routing groups, represented by IFaxOutboundRoutingGroup interfaces.
helpviewer_keywords: ["IFaxOutboundRoutingGroups","IFaxOutboundRoutingGroups interface [Fax Service]","IFaxOutboundRoutingGroups interface [Fax Service]","described","_mfax_faxoutboundroutinggroups_cpp","fax._mfax_faxoutboundroutinggroups_cpp","faxcomex/IFaxOutboundRoutingGroups"]
old-location: fax\_mfax_faxoutboundroutinggroups_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_62r7_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingGroups, IFaxOutboundRoutingGroups interface [Fax Service], IFaxOutboundRoutingGroups interface [Fax Service],described, _mfax_faxoutboundroutinggroups_cpp, fax._mfax_faxoutboundroutinggroups_cpp, faxcomex/IFaxOutboundRoutingGroups
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutboundRoutingGroups
 - faxcomex/IFaxOutboundRoutingGroups
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutboundRoutingGroups
---

# IFaxOutboundRoutingGroups interface


## -description

The <b>IFaxOutboundRoutingGroups</b> interface describes a configuration collection used by a fax client application to manage the fax outbound routing groups, represented by <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroup">IFaxOutboundRoutingGroup</a> interfaces. The interface also includes methods to add and remove groups from the collection.
<div class="alert"><b>Note</b>  The outbound routing group <b>All Devices</b> is always the first object in this collection. You cannot remove the <b>All Devices</b> group from the collection. If you attempt to remove it, you will receive an error message.
</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRoutingGroups</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutboundRoutingGroups</b> also has these types of members:
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
<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutinggroups-add">Add</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutinggroups-add">IFaxOutboundRoutingGroups::Add</a> method adds an outbound routing group to the collection represented by the <b>IFaxOutboundRoutingGroups</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutinggroups-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutinggroups-get__newenum">IFaxOutboundRoutingGroups::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups">FaxOutboundRoutingGroups</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutinggroups-get_item">Item</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutinggroups-get_item">IFaxOutboundRoutingGroups::get_Item</a> method returns a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroup">IFaxOutboundRoutingGroup</a> interface from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups-remove-vb">Remove</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups-remove-vb">Remove</a> method removes an item from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups">FaxOutboundRoutingGroups</a> collection. 

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

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups-count-vb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups-count-vb">Count</a> property represents the number of objects in the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups">FaxOutboundRoutingGroups</a> collection. This is the total number of outbound routing groups associated with the fax server.

</td>
</tr>
</table>

## -remarks

A default implementation of <b>IFaxOutboundRoutingGroups</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups">FaxOutboundRoutingGroups</a> object.