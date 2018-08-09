---
UID: NN:faxcomex.IFaxOutboundRoutingRules
title: IFaxOutboundRoutingRules
author: windows-sdk-content
description: The IFaxOutboundRoutingRules interface describes a configuration collection that is used by a fax client application to manage the fax outbound routing rules.
old-location: fax\_mfax_faxoutboundroutingrules_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_69f7_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxOutboundRoutingRules, IFaxOutboundRoutingRules interface [Fax Service], IFaxOutboundRoutingRules interface [Fax Service],described, _mfax_faxoutboundroutingrules_cpp, fax._mfax_faxoutboundroutingrules_cpp, faxcomex/IFaxOutboundRoutingRules
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRoutingRules interface


## -description


The <b>IFaxOutboundRoutingRules</b> interface describes a configuration collection that is used by a fax client application to manage the fax outbound routing rules. The collection also includes methods to add and remove rules from the collection. Each outbound routing rule is represented by a <a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a> interface.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRoutingRules</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutboundRoutingRules</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3588272c-13c1-4bd4-96d2-19289a2ee07d">IFaxOutboundRoutingRules::Add</a> method adds an outbound routing rule (<a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a> interface) to the collection defined by the <b>IFaxOutboundRoutingRules</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db31319a-d998-4b7a-a037-ae739fb190b4">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/db31319a-d998-4b7a-a037-ae739fb190b4">IFaxOutboundRoutingRules::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6463b423-af8c-4d35-badb-4ea7e749875e">IFaxOutboundRoutingRules::get_Item</a> method returns a <a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a> interface from the <b>IFaxOutboundRoutingRules</b> interface using the routing rule's index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/776a52cc-2e17-4443-b0a5-e16acc0d393e">ItemByCountryAndArea</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/776a52cc-2e17-4443-b0a5-e16acc0d393e">IFaxOutboundRoutingRules::get_ItemByCountryAndArea</a> method returns an outbound routing rule (<a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object) from the collection using the routing rule's country/region code and area code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ed1221a2-f3dc-46fb-b05c-8af85ba5a142">IFaxOutboundRoutingRules::Remove</a> method removes an outbound routing rule (<a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object) from the <a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a> collection using the routing rule's index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5776e1e4-fa77-4c00-99ac-df8b56f9dbc4">RemoveByCountryAndArea</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5776e1e4-fa77-4c00-99ac-df8b56f9dbc4">IFaxOutboundRoutingRules::RemoveByCountryAndArea</a> method removes an outbound routing rule (<a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object) from the collection using the routing rule's country/region code and area code.

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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3add9157-b82a-4046-ad20-f6a29f92257e">IFaxOutboundRoutingRules::get_Count</a> property represents the number of objects in the <a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a> collection. This is the total number of outbound routing rules associated with the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutboundRoutingRules</b> is provided as the <a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a> object.



