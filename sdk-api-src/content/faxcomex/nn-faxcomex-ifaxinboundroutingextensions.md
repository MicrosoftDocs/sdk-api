---
UID: NN:faxcomex.IFaxInboundRoutingExtensions
title: IFaxInboundRoutingExtensions
author: windows-sdk-content
description: The IFaxInboundRoutingExtensions interface defines a configuration collection used by a fax client application to manage the inbound fax routing extensions registered with the fax service.
old-location: fax\_mfax_faxinboundroutingextensions_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1v1v_cpp.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxInboundRoutingExtensions, IFaxInboundRoutingExtensions interface [Fax Service], IFaxInboundRoutingExtensions interface [Fax Service],described, _mfax_faxinboundroutingextensions_cpp, fax._mfax_faxinboundroutingextensions_cpp, faxcomex/IFaxInboundRoutingExtensions
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
 - IFaxInboundRoutingExtensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRoutingExtensions interface


## -description


The <b>IFaxInboundRoutingExtensions</b> interface defines a configuration collection used by a fax client application to manage the inbound fax routing extensions registered with the fax service. Each extension is represented by a <a href="https://msdn.microsoft.com/en-us/library/ms684580(v=VS.85).aspx">FaxInboundRoutingExtension</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingExtensions</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxInboundRoutingExtensions</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms687481(v=VS.85).aspx">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687481(v=VS.85).aspx">IFaxInboundRoutingExtensions::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <b>IFaxInboundRoutingExtensions</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687505(v=VS.85).aspx">Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687505(v=VS.85).aspx">IFaxInboundRoutingExtensions::get_Item</a> method returns a <a href="https://msdn.microsoft.com/en-us/library/ms684581(v=VS.85).aspx">IFaxInboundRoutingExtension</a> interface from the <b>IFaxInboundRoutingExtensions</b> collection.

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

<a href="https://msdn.microsoft.com/en-us/library/ms685078(v=VS.85).aspx">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685078(v=VS.85).aspx">IFaxInboundRoutingExtensions::get_Count</a> property represents the number of objects in the <b>IFaxInboundRoutingExtensions</b> collection. This is the total number of inbound routing extensions associated with the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRoutingExtensions</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms684899(v=VS.85).aspx">FaxInboundRoutingExtensions</a> object.



