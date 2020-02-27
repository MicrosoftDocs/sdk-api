---
UID: NN:faxcomex.IFaxOutboundRouting
title: IFaxOutboundRouting (faxcomex.h)
description: The IFaxOutboundRouting interface defines a configuration object that is used by a fax client application to configure the outbound routing groups (IFaxOutboundRoutingGroups interfaces) and outbound routing rules (IFaxOutboundRoutingRules interfaces).
old-location: fax\_mfax_faxoutboundrouting_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8nhj_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRouting, IFaxOutboundRouting interface [Fax Service], IFaxOutboundRouting interface [Fax Service],described, _mfax_faxoutboundrouting_cpp, fax._mfax_faxoutboundrouting_cpp, faxcomex/IFaxOutboundRouting
f1_keywords:
- faxcomex/IFaxOutboundRouting
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutboundRouting interface


## -description


The <b>IFaxOutboundRouting</b> interface defines a configuration object that is used by a fax client application to configure the outbound routing groups (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroups">IFaxOutboundRoutingGroups</a> interfaces) and outbound routing rules (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a> interfaces).
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutboundRouting</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutboundRouting</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundrouting-getgroups">GetGroups</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundrouting-getgroups">IFaxOutboundRouting::GetGroups</a> method retrieves an interface that represents a collection of outbound routing groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundrouting-getrules">GetRules</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutboundrouting-getrules">IFaxOutboundRouting::GetRules</a> method retrieves an interface that represents a collection of outbound routing groups.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutboundRouting</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutboundrouting">FaxOutboundRouting</a> object.



