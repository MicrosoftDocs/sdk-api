---
UID: NN:faxcomex.IFaxInboundRoutingMethod
title: IFaxInboundRoutingMethod (faxcomex.h)
description: The IFaxInboundRoutingMethod interface defines a configuration object used by a fax client application to retrieve information about an individual fax inbound routing method on a connected fax server.
helpviewer_keywords: ["IFaxInboundRoutingMethod","IFaxInboundRoutingMethod interface [Fax Service]","IFaxInboundRoutingMethod interface [Fax Service]","described","_mfax_faxinboundroutingmethod_cpp","fax._mfax_faxinboundroutingmethod_cpp","faxcomex/IFaxInboundRoutingMethod"]
old-location: fax\_mfax_faxinboundroutingmethod_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_95t0_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxInboundRoutingMethod, IFaxInboundRoutingMethod interface [Fax Service], IFaxInboundRoutingMethod interface [Fax Service],described, _mfax_faxinboundroutingmethod_cpp, fax._mfax_faxinboundroutingmethod_cpp, faxcomex/IFaxInboundRoutingMethod
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
 - IFaxInboundRoutingMethod
 - faxcomex/IFaxInboundRoutingMethod
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
 - IFaxInboundRoutingMethod
---

# IFaxInboundRoutingMethod interface


## -description

The <b>IFaxInboundRoutingMethod</b> interface defines a configuration object used by a fax client application to retrieve information about an individual fax inbound routing method on a connected fax server.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingMethod</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxInboundRoutingMethod</b> also has these types of members:
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
<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-refresh-vb">IFaxInboundRoutingMethod::Refresh</a> method refreshes <b>IFaxInboundRoutingMethod</b> interface information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-save-vb">Save</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-save-vb">IFaxInboundRoutingMethod::Save</a> method saves the <b>IFaxInboundRoutingMethod</b> interface's data.

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

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-extensionfriendlyname-vb">ExtensionFriendlyName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-extensionfriendlyname-vb">IFaxInboundRoutingMethod::get_ExtensionFriendlyName</a> property is the user-friendly name for the fax routing extension that exports the inbound fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-extensionimagename-vb">ExtensionImageName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-extensionimagename-vb">IFaxInboundRoutingMethod::get_ExtensionImageName</a> property is a null-terminated string that contains the executable image name (DLL path and file name) of the fax routing extension that exports the fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-functionname-vb">FunctionName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-functionname-vb">IFaxInboundRoutingMethod::get_FunctionName</a> property is a null-terminated string that contains the name of the function that executes a specific fax routing procedure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-guid-vb">GUID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-guid-vb">IFaxInboundRoutingMethod::get_GUID</a> property is a null-terminated string that specifies the GUID that uniquely identifies the fax routing method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-name-vb">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-name-vb">IFaxInboundRoutingMethod::get_Name</a> property is a null-terminated string that contains the user-friendly name associated with the inbound fax routing method. The string is suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxinboundroutingmethod-get_priority">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-priority">Priority</a> property is a value associated with the order in which the fax service calls the routing method when the service receives a fax job.

</td>
</tr>
</table>

## -remarks

A default implementation of <b>IFaxInboundRoutingMethod</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod">FaxInboundRoutingMethod</a> object.