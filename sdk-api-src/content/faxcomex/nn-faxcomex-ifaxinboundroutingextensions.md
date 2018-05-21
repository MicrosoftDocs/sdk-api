---
UID: NN:faxcomex.IFaxInboundRoutingExtensions
title: IFaxInboundRoutingExtensions
author: windows-driver-content
description: The IFaxInboundRoutingExtensions interface defines a configuration collection used by a fax client application to manage the inbound fax routing extensions registered with the fax service.
old-location: fax\_mfax_faxinboundroutingextensions_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1v1v_cpp.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFaxInboundRoutingExtensions, IFaxInboundRoutingExtensions interface [Fax Service], IFaxInboundRoutingExtensions interface [Fax Service],described, _mfax_faxinboundroutingextensions_cpp, fax._mfax_faxinboundroutingextensions_cpp, faxcomex/IFaxInboundRoutingExtensions
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
-	IFaxInboundRoutingExtensions
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxInboundRoutingExtensions interface


## -description


The <b>IFaxInboundRoutingExtensions</b> interface defines a configuration collection used by a fax client application to manage the inbound fax routing extensions registered with the fax service. Each extension is represented by a <a href="https://msdn.microsoft.com/cb875610-d6c9-473d-b9c2-0035e67a8949">FaxInboundRoutingExtension</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingExtensions</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxInboundRoutingExtensions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxInboundRoutingExtensions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe42a4e2-699d-4a34-b636-479d2a85f34b">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fe42a4e2-699d-4a34-b636-479d2a85f34b">IFaxInboundRoutingExtensions::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <b>IFaxInboundRoutingExtensions</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b647f803-5979-44af-828f-f853b716ecf5">IFaxInboundRoutingExtensions::get_Item</a> method returns a <a href="https://msdn.microsoft.com/e967c113-a4c0-4a83-949b-eb51fe41fb42">IFaxInboundRoutingExtension</a> interface from the <b>IFaxInboundRoutingExtensions</b> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingExtensions</b> interface has these properties.
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
The <a href="https://msdn.microsoft.com/12ab8005-c1e3-41fb-a02b-36b84d1726bb">IFaxInboundRoutingExtensions::get_Count</a> property represents the number of objects in the <b>IFaxInboundRoutingExtensions</b> collection. This is the total number of inbound routing extensions associated with the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRoutingExtensions</b> is provided as the <a href="https://msdn.microsoft.com/8989c149-bbf4-46c1-b969-949d44efcf90">FaxInboundRoutingExtensions</a> object.



