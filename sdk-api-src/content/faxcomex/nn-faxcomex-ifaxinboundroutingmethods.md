---
UID: NN:faxcomex.IFaxInboundRoutingMethods
title: IFaxInboundRoutingMethods (faxcomex.h)
description: The IFaxInboundRoutingMethods interface defines a configuration collection used by a fax client application to manage the ordered inbound fax routing methods.
old-location: fax\_mfax_faxinboundroutingmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6bn7_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxInboundRoutingMethods, IFaxInboundRoutingMethods interface [Fax Service], IFaxInboundRoutingMethods interface [Fax Service],described, _mfax_faxinboundroutingmethods_cpp, fax._mfax_faxinboundroutingmethods_cpp, faxcomex/IFaxInboundRoutingMethods
f1_keywords:
- faxcomex/IFaxInboundRoutingMethods
dev_langs:
- c++
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
- IFaxInboundRoutingMethods
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxInboundRoutingMethods interface


## -description


The <b>IFaxInboundRoutingMethods</b> interface defines a configuration collection used by a fax client application to manage the ordered inbound fax routing methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingMethods</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxInboundRoutingMethods</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxInboundRoutingMethods</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxinboundroutingmethods-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxinboundroutingmethods-get__newenum">IFaxInboundRoutingMethods::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <b>IFaxInboundRoutingMethods</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxinboundroutingmethods-get_item">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxinboundroutingmethods-get_item">IFaxInboundRoutingMethods::get_Item</a> method returns a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethod">IFaxInboundRoutingMethod</a> object from the <b>IFaxInboundRoutingMethods</b> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingMethods</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethods-count-vb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethods-count-vb">IFaxInboundRoutingMethods::get_Count</a> property represents the number of objects in the <b>IFaxInboundRoutingMethods</b> collection. This is the total number of inbound routing methods associated with the fax server.

</td>
</tr>
</table> 


## -remarks



Each inbound routing method is represented by a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethod">IFaxInboundRoutingMethod</a> interface. The order of the routing methods in the collection determines the relative order in which the methods execute when an inbound fax requires routing.

A default implementation of <b>IFaxInboundRoutingMethods</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethods">FaxInboundRoutingMethods</a> object.



