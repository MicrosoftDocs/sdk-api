---
UID: NN:faxcomex.IFaxOutboundRoutingRules
title: IFaxOutboundRoutingRules (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutboundRoutingRules interface describes a configuration collection that is used by a fax client application to manage the fax outbound routing rules.
old-location: fax\_mfax_faxoutboundroutingrules_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_69f7_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingRules, IFaxOutboundRoutingRules interface [Fax Service], IFaxOutboundRoutingRules interface [Fax Service],described, _mfax_faxoutboundroutingrules_cpp, fax._mfax_faxoutboundroutingrules_cpp, faxcomex/IFaxOutboundRoutingRules
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxOutboundRoutingRules"
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
 - IFaxOutboundRoutingRules
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutboundRoutingRules interface


## -description


The <b>IFaxOutboundRoutingRules</b> interface describes a configuration collection that is used by a fax client application to manage the fax outbound routing rules. The collection also includes methods to add and remove rules from the collection. Each outbound routing rule is represented by a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a> interface.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRoutingRules</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutboundRoutingRules</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutboundRoutingRules</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutingrules-add">Add</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutingrules-add">IFaxOutboundRoutingRules::Add</a> method adds an outbound routing rule (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a> interface) to the collection defined by the <b>IFaxOutboundRoutingRules</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutingrules-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutingrules-get__newenum">IFaxOutboundRoutingRules::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutingrules-get_item">Item</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundroutingrules-get_item">IFaxOutboundRoutingRules::get_Item</a> method returns a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a> interface from the <b>IFaxOutboundRoutingRules</b> interface using the routing rule's index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-itembycountryandarea-vb">ItemByCountryAndArea</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-itembycountryandarea-vb">IFaxOutboundRoutingRules::get_ItemByCountryAndArea</a> method returns an outbound routing rule (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a> object) from the collection using the routing rule's country/region code and area code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-remove-vb">Remove</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-remove-vb">IFaxOutboundRoutingRules::Remove</a> method removes an outbound routing rule (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a> object) from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a> collection using the routing rule's index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-removebycountryandarea-vb">RemoveByCountryAndArea</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-removebycountryandarea-vb">IFaxOutboundRoutingRules::RemoveByCountryAndArea</a> method removes an outbound routing rule (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a> object) from the collection using the routing rule's country/region code and area code.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRoutingRules</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-count-vb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-count-vb">IFaxOutboundRoutingRules::get_Count</a> property represents the number of objects in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a> collection. This is the total number of outbound routing rules associated with the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutboundRoutingRules</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a> object.



