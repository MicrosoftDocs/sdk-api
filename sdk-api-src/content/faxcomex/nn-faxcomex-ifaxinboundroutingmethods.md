---
UID: NN:faxcomex.IFaxInboundRoutingMethods
title: IFaxInboundRoutingMethods
author: windows-driver-content
description: The IFaxInboundRoutingMethods interface defines a configuration collection used by a fax client application to manage the ordered inbound fax routing methods.
old-location: fax\_mfax_faxinboundroutingmethods_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6bn7_cpp.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxInboundRoutingMethods, IFaxInboundRoutingMethods interface [Fax Service], IFaxInboundRoutingMethods interface [Fax Service],described, _mfax_faxinboundroutingmethods_cpp, fax._mfax_faxinboundroutingmethods_cpp, faxcomex/IFaxInboundRoutingMethods
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxInboundRoutingMethods
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxInboundRoutingMethods interface


## -description


The <b>IFaxInboundRoutingMethods</b> interface defines a configuration collection used by a fax client application to manage the ordered inbound fax routing methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingMethods</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxInboundRoutingMethods</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b2ee772f-2f69-4d3c-9934-f4ce677834d4">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b2ee772f-2f69-4d3c-9934-f4ce677834d4">IFaxInboundRoutingMethods::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <b>IFaxInboundRoutingMethods</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb4feb73-1a0e-474a-bd37-1dce6608a816">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fb4feb73-1a0e-474a-bd37-1dce6608a816">IFaxInboundRoutingMethods::get_Item</a> method returns a <a href="https://msdn.microsoft.com/ca33c439-24e7-4b85-8e29-a0a0176f0ae2">IFaxInboundRoutingMethod</a> object from the <b>IFaxInboundRoutingMethods</b> collection.

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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6a5f99b5-bf1c-45bd-80ad-2a9ee30c58f8">IFaxInboundRoutingMethods::get_Count</a> property represents the number of objects in the <b>IFaxInboundRoutingMethods</b> collection. This is the total number of inbound routing methods associated with the fax server.

</td>
</tr>
</table> 


## -remarks



Each inbound routing method is represented by a <a href="https://msdn.microsoft.com/ca33c439-24e7-4b85-8e29-a0a0176f0ae2">IFaxInboundRoutingMethod</a> interface. The order of the routing methods in the collection determines the relative order in which the methods execute when an inbound fax requires routing.

A default implementation of <b>IFaxInboundRoutingMethods</b> is provided as the <a href="https://msdn.microsoft.com/5a00a56f-f82b-4e4b-b78f-d9f7417090c8">FaxInboundRoutingMethods</a> object.



