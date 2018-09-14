---
UID: NN:faxcomex.IFaxInboundRouting
title: IFaxInboundRouting
author: windows-sdk-content
description: The IFaxInboundRouting interface defines a configuration object used by a fax client application to access the inbound routing extensions registered with the fax service, represented by FaxInboundRoutingExtensions objects, and the routing methods the extensions expose, represented by FaxInboundRoutingMethods objects.
old-location: fax\_mfax_faxinboundrouting_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0zc7_cpp.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxInboundRouting, IFaxInboundRouting interface [Fax Service], IFaxInboundRouting interface [Fax Service],described, _mfax_faxinboundrouting_cpp, fax._mfax_faxinboundrouting_cpp, faxcomex/IFaxInboundRouting
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
 - IFaxInboundRouting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRouting interface


## -description


The <b>IFaxInboundRouting</b> interface defines a configuration object used by a fax client application to access the inbound routing extensions registered with the fax service, represented by <a href="https://msdn.microsoft.com/8989c149-bbf4-46c1-b969-949d44efcf90">FaxInboundRoutingExtensions</a> objects, and the routing methods the extensions expose, represented by <a href="https://msdn.microsoft.com/5a00a56f-f82b-4e4b-b78f-d9f7417090c8">FaxInboundRoutingMethods</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRouting</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxInboundRouting</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8e82da40-5830-4997-96e6-3551101bdd54">GetExtensions</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ecd9a5bb-1624-4cfe-a2d9-b9a5ed722fc4">GetExtensions</a> method retrieves the collection of inbound routing extensions registered with the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/532f54a0-a3c7-4f99-9add-89474aa2fe86">GetMethods</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/532f54a0-a3c7-4f99-9add-89474aa2fe86">IFaxInboundRouting::GetMethods</a> method retrieves the ordered collection of all the inbound routing methods exposed by all the inbound routing extensions currently registered with the fax service.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRouting</b> is provided as the <a href="https://msdn.microsoft.com/4cf71225-fcd8-4d2f-b8b3-acbb32708f3b">FaxInboundRouting</a> object.



