---
UID: NN:faxcomex.IFaxOutboundRouting
title: IFaxOutboundRouting
author: windows-sdk-content
description: The IFaxOutboundRouting interface defines a configuration object that is used by a fax client application to configure the outbound routing groups (IFaxOutboundRoutingGroups interfaces) and outbound routing rules (IFaxOutboundRoutingRules interfaces).
old-location: fax\_mfax_faxoutboundrouting_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8nhj_cpp.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IFaxOutboundRouting, IFaxOutboundRouting interface [Fax Service], IFaxOutboundRouting interface [Fax Service],described, _mfax_faxoutboundrouting_cpp, fax._mfax_faxoutboundrouting_cpp, faxcomex/IFaxOutboundRouting
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
 - IFaxOutboundRouting
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRouting interface


## -description


The <b>IFaxOutboundRouting</b> interface defines a configuration object that is used by a fax client application to configure the outbound routing groups (<a href="https://msdn.microsoft.com/cf36787b-cc8e-48a8-b81d-5406cbc4bcc8">IFaxOutboundRoutingGroups</a> interfaces) and outbound routing rules (<a href="https://msdn.microsoft.com/bd059904-b5b6-4485-a64e-0beaa4de7379">IFaxOutboundRoutingRules</a> interfaces).
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRouting</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutboundRouting</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxOutboundRouting</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13a1cb1b-9953-401c-ba09-1ba030ffd470">GetGroups</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/13a1cb1b-9953-401c-ba09-1ba030ffd470">IFaxOutboundRouting::GetGroups</a> method retrieves an interface that represents a collection of outbound routing groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e359c02-2f44-4d97-a354-3e7190e0936b">GetRules</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8e359c02-2f44-4d97-a354-3e7190e0936b">IFaxOutboundRouting::GetRules</a> method retrieves an interface that represents a collection of outbound routing groups.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutboundRouting</b> is provided as the <a href="https://msdn.microsoft.com/64ff05d6-6ebe-4155-96cd-7b925c979492">FaxOutboundRouting</a> object.



