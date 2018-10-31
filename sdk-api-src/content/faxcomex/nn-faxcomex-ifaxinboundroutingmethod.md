---
UID: NN:faxcomex.IFaxInboundRoutingMethod
title: IFaxInboundRoutingMethod
author: windows-sdk-content
description: The IFaxInboundRoutingMethod interface defines a configuration object used by a fax client application to retrieve information about an individual fax inbound routing method on a connected fax server.
old-location: fax\_mfax_faxinboundroutingmethod_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_95t0_cpp.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFaxInboundRoutingMethod, IFaxInboundRoutingMethod interface [Fax Service], IFaxInboundRoutingMethod interface [Fax Service],described, _mfax_faxinboundroutingmethod_cpp, fax._mfax_faxinboundroutingmethod_cpp, faxcomex/IFaxInboundRoutingMethod
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingMethod</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxInboundRoutingMethod</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f13d17ea-f73b-4f32-83c5-f1b0b9e71464">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f13d17ea-f73b-4f32-83c5-f1b0b9e71464">IFaxInboundRoutingMethod::Refresh</a> method refreshes <b>IFaxInboundRoutingMethod</b> interface information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fd645f1-9162-46ea-89a9-0888d86ec187">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7fd645f1-9162-46ea-89a9-0888d86ec187">IFaxInboundRoutingMethod::Save</a> method saves the <b>IFaxInboundRoutingMethod</b> interface's data.

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

<a href="https://msdn.microsoft.com/29f01792-bb13-4ff1-9ad4-6790c9dfd1af">ExtensionFriendlyName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/29f01792-bb13-4ff1-9ad4-6790c9dfd1af">IFaxInboundRoutingMethod::get_ExtensionFriendlyName</a> property is the user-friendly name for the fax routing extension that exports the inbound fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/33be2539-5477-4e56-8347-a80c5cfa77e7">ExtensionImageName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/33be2539-5477-4e56-8347-a80c5cfa77e7">IFaxInboundRoutingMethod::get_ExtensionImageName</a> property is a null-terminated string that contains the executable image name (DLL path and file name) of the fax routing extension that exports the fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2dcc5ff2-3bb1-4f66-90f4-ba1991714575">FunctionName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2dcc5ff2-3bb1-4f66-90f4-ba1991714575">IFaxInboundRoutingMethod::get_FunctionName</a> property is a null-terminated string that contains the name of the function that executes a specific fax routing procedure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bb6d674d-d506-4c9e-8858-c9ce40912d72">GUID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bb6d674d-d506-4c9e-8858-c9ce40912d72">IFaxInboundRoutingMethod::get_GUID</a> property is a null-terminated string that specifies the GUID that uniquely identifies the fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/920f4b67-b216-4056-a109-36ed5d8bc556">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/920f4b67-b216-4056-a109-36ed5d8bc556">IFaxInboundRoutingMethod::get_Name</a> property is a null-terminated string that contains the user-friendly name associated with the inbound fax routing method. The string is suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/01db2b72-67a9-4f1a-bdde-228310da519d">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/23208ac4-68c8-4f62-b588-2d0a5575f87c">Priority</a> property is a value associated with the order in which the fax service calls the routing method when the service receives a fax job.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRoutingMethod</b> is provided as the <a href="https://msdn.microsoft.com/8eb68201-4c87-41ce-a401-a039b5ad454d">FaxInboundRoutingMethod</a> object.



