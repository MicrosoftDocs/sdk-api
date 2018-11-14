---
UID: NN:faxcomex.IFaxOutboundRouting
title: IFaxOutboundRouting
author: windows-sdk-content
description: The IFaxOutboundRouting interface defines a configuration object that is used by a fax client application to configure the outbound routing groups (IFaxOutboundRoutingGroups interfaces) and outbound routing rules (IFaxOutboundRoutingRules interfaces).
old-location: fax\_mfax_faxoutboundrouting_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8nhj_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutboundRouting, IFaxOutboundRouting interface [Fax Service], IFaxOutboundRouting interface [Fax Service],described, _mfax_faxoutboundrouting_cpp, fax._mfax_faxoutboundrouting_cpp, faxcomex/IFaxOutboundRouting
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
 - IFaxOutboundRouting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRouting interface


## -description


The <b>IFaxOutboundRouting</b> interface defines a configuration object that is used by a fax client application to configure the outbound routing groups (<a href="https://msdn.microsoft.com/en-us/library/ms689212(v=VS.85).aspx">IFaxOutboundRoutingGroups</a> interfaces) and outbound routing rules (<a href="https://msdn.microsoft.com/en-us/library/ms689527(v=VS.85).aspx">IFaxOutboundRoutingRules</a> interfaces).
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRouting</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxOutboundRouting</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms690115(v=VS.85).aspx">GetGroups</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690115(v=VS.85).aspx">IFaxOutboundRouting::GetGroups</a> method retrieves an interface that represents a collection of outbound routing groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688524(v=VS.85).aspx">GetRules</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688524(v=VS.85).aspx">IFaxOutboundRouting::GetRules</a> method retrieves an interface that represents a collection of outbound routing groups.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutboundRouting</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms690136(v=VS.85).aspx">FaxOutboundRouting</a> object.



