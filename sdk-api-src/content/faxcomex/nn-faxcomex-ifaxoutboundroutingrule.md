---
UID: NN:faxcomex.IFaxOutboundRoutingRule
title: IFaxOutboundRoutingRule
author: windows-sdk-content
description: The IFaxOutboundRoutingRule interface describes a configuration object that is used by a fax client application to set and retrieve information about an individual fax outbound routing rule.
old-location: fax\_mfax_faxoutboundroutingrule_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9mn9_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxOutboundRoutingRule, IFaxOutboundRoutingRule interface [Fax Service], IFaxOutboundRoutingRule interface [Fax Service],described, _mfax_faxoutboundroutingrule_cpp, fax._mfax_faxoutboundroutingrule_cpp, faxcomex/IFaxOutboundRoutingRule
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.redist: 
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
 - IFaxOutboundRoutingRule
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRoutingRule interface


## -description


The <b>IFaxOutboundRoutingRule</b> interface describes a configuration object that is used by a fax client application to set and retrieve information about an individual fax outbound routing rule.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRoutingRule</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutboundRoutingRule</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutboundRoutingRule</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b104dfb9-6feb-48c3-b3ef-f91b78f647c4">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b104dfb9-6feb-48c3-b3ef-f91b78f647c4">IFaxOutboundRoutingRule::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fd084a6-3b74-4e6a-8656-de934e75e923">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5fd084a6-3b74-4e6a-8656-de934e75e923">IFaxOutboundRoutingRule::Save</a> method saves the <a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRoutingRule</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7863cd01-956e-4ec8-952b-9b13e88e859c">AreaCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7863cd01-956e-4ec8-952b-9b13e88e859c">IFaxOutboundRoutingRule::get_AreaCode</a> property specifies the area code to which the outbound routing rule applies.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/67cc223a-c772-443b-b371-63f29acf8a67">CountryCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/67cc223a-c772-443b-b371-63f29acf8a67">IFaxOutboundRoutingRule::get_CountryCode</a> property specifies the country/region code to which the outbound routing rule applies.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b655a85a-e817-49d4-8647-8f5c4e101c7b">DeviceId</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b655a85a-e817-49d4-8647-8f5c4e101c7b">IFaxOutboundRoutingRule::get_DeviceId</a> property specifies the device ID if the outbound routing rule points to a single fax device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/06c3ed15-4b1f-4e50-bccf-ab02c0b2dbaa">GroupName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/06c3ed15-4b1f-4e50-bccf-ab02c0b2dbaa">IFaxOutboundRoutingRule::get_GroupName</a> property specifies the group name if the outbound routing rule points to a group of fax devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5a880005-92a2-4809-b64c-b5af63382203">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5a880005-92a2-4809-b64c-b5af63382203">IFaxOutboundRoutingRule::get_Status</a> property indicates the current status of the outbound routing rule; for example, whether the rule is valid and whether it can apply to fax jobs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/64b1778a-a53f-468b-8ec0-93db23036730">UseDevice</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/64b1778a-a53f-468b-8ec0-93db23036730">IFaxOutboundRoutingRule::get_UseDevice</a> property is a Boolean value that indicates whether the outbound routing rule points to a single fax device.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutboundRoutingRule</b> is provided as the <a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object.



