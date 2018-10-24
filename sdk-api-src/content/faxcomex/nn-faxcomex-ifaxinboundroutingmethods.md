---
UID: NN:faxcomex.IFaxInboundRoutingMethods
title: IFaxInboundRoutingMethods
author: windows-sdk-content
description: The IFaxInboundRoutingMethods interface defines a configuration collection used by a fax client application to manage the ordered inbound fax routing methods.
old-location: fax\_mfax_faxinboundroutingmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6bn7_cpp.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxInboundRoutingMethods, IFaxInboundRoutingMethods interface [Fax Service], IFaxInboundRoutingMethods interface [Fax Service],described, _mfax_faxinboundroutingmethods_cpp, fax._mfax_faxinboundroutingmethods_cpp, faxcomex/IFaxInboundRoutingMethods
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRoutingMethods interface


## -description


The <b>IFaxInboundRoutingMethods</b> interface defines a configuration collection used by a fax client application to manage the ordered inbound fax routing methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingMethods</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxInboundRoutingMethods</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms685132(v=VS.85).aspx">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685132(v=VS.85).aspx">IFaxInboundRoutingMethods::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <b>IFaxInboundRoutingMethods</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686742(v=VS.85).aspx">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686742(v=VS.85).aspx">IFaxInboundRoutingMethods::get_Item</a> method returns a <a href="https://msdn.microsoft.com/en-us/library/ms687470(v=VS.85).aspx">IFaxInboundRoutingMethod</a> object from the <b>IFaxInboundRoutingMethods</b> collection.

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

<a href="https://msdn.microsoft.com/en-us/library/ms687467(v=VS.85).aspx">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687467(v=VS.85).aspx">IFaxInboundRoutingMethods::get_Count</a> property represents the number of objects in the <b>IFaxInboundRoutingMethods</b> collection. This is the total number of inbound routing methods associated with the fax server.

</td>
</tr>
</table> 


## -remarks



Each inbound routing method is represented by a <a href="https://msdn.microsoft.com/en-us/library/ms687470(v=VS.85).aspx">IFaxInboundRoutingMethod</a> interface. The order of the routing methods in the collection determines the relative order in which the methods execute when an inbound fax requires routing.

A default implementation of <b>IFaxInboundRoutingMethods</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms686674(v=VS.85).aspx">FaxInboundRoutingMethods</a> object.



