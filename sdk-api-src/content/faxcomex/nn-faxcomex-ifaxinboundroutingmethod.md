---
UID: NN:faxcomex.IFaxInboundRoutingMethod
title: IFaxInboundRoutingMethod
author: windows-sdk-content
description: The IFaxInboundRoutingMethod interface defines a configuration object used by a fax client application to retrieve information about an individual fax inbound routing method on a connected fax server.
old-location: fax\_mfax_faxinboundroutingmethod_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_95t0_cpp.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxInboundRoutingMethod, IFaxInboundRoutingMethod interface [Fax Service], IFaxInboundRoutingMethod interface [Fax Service],described, _mfax_faxinboundroutingmethod_cpp, fax._mfax_faxinboundroutingmethod_cpp, faxcomex/IFaxInboundRoutingMethod
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
 - IFaxInboundRoutingMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRoutingMethod interface


## -description


The <b>IFaxInboundRoutingMethod</b> interface defines a configuration object used by a fax client application to retrieve information about an individual fax inbound routing method on a connected fax server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingMethod</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxInboundRoutingMethod</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxInboundRoutingMethod</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686042(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686042(v=VS.85).aspx">IFaxInboundRoutingMethod::Refresh</a> method refreshes <b>IFaxInboundRoutingMethod</b> interface information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684815(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684815(v=VS.85).aspx">IFaxInboundRoutingMethod::Save</a> method saves the <b>IFaxInboundRoutingMethod</b> interface's data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingMethod</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686194(v=VS.85).aspx">ExtensionFriendlyName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686194(v=VS.85).aspx">IFaxInboundRoutingMethod::get_ExtensionFriendlyName</a> property is the user-friendly name for the fax routing extension that exports the inbound fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686486(v=VS.85).aspx">ExtensionImageName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686486(v=VS.85).aspx">IFaxInboundRoutingMethod::get_ExtensionImageName</a> property is a null-terminated string that contains the executable image name (DLL path and file name) of the fax routing extension that exports the fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686911(v=VS.85).aspx">FunctionName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686911(v=VS.85).aspx">IFaxInboundRoutingMethod::get_FunctionName</a> property is a null-terminated string that contains the name of the function that executes a specific fax routing procedure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686469(v=VS.85).aspx">GUID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686469(v=VS.85).aspx">IFaxInboundRoutingMethod::get_GUID</a> property is a null-terminated string that specifies the GUID that uniquely identifies the fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685341(v=VS.85).aspx">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685341(v=VS.85).aspx">IFaxInboundRoutingMethod::get_Name</a> property is a null-terminated string that contains the user-friendly name associated with the inbound fax routing method. The string is suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686151(v=VS.85).aspx">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686150(v=VS.85).aspx">Priority</a> property is a value associated with the order in which the fax service calls the routing method when the service receives a fax job.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRoutingMethod</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms687469(v=VS.85).aspx">FaxInboundRoutingMethod</a> object.



