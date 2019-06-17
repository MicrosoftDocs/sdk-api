---
UID: NN:faxcomex.IFaxInboundRouting
title: IFaxInboundRouting (faxcomex.h)
author: windows-sdk-content
description: The IFaxInboundRouting interface defines a configuration object used by a fax client application to access the inbound routing extensions registered with the fax service, represented by FaxInboundRoutingExtensions objects, and the routing methods the extensions expose, represented by FaxInboundRoutingMethods objects.
old-location: fax\_mfax_faxinboundrouting_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0zc7_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxInboundRouting, IFaxInboundRouting interface [Fax Service], IFaxInboundRouting interface [Fax Service],described, _mfax_faxinboundrouting_cpp, fax._mfax_faxinboundrouting_cpp, faxcomex/IFaxInboundRouting
ms.topic: interface
f1_keywords: ["faxcomex/IFaxInboundRouting"]
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
 - IFaxInboundRouting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxInboundRouting interface


## -description


The <b>IFaxInboundRouting</b> interface defines a configuration object used by a fax client application to access the inbound routing extensions registered with the fax service, represented by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextensions">FaxInboundRoutingExtensions</a> objects, and the routing methods the extensions expose, represented by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethods">FaxInboundRoutingMethods</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRouting</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxInboundRouting</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxInboundRouting</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxinboundrouting-getextensions">GetExtensions</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundrouting-getextensions">GetExtensions</a> method retrieves the collection of inbound routing extensions registered with the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxinboundrouting-getmethods">GetMethods</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxinboundrouting-getmethods">IFaxInboundRouting::GetMethods</a> method retrieves the ordered collection of all the inbound routing methods exposed by all the inbound routing extensions currently registered with the fax service.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRouting</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundrouting">FaxInboundRouting</a> object.



