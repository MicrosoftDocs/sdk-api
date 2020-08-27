---
UID: NN:xpsobjectmodel.IXpsOMPrintTicketResource
title: IXpsOMPrintTicketResource (xpsobjectmodel.h)
description: Provides an IStream interface to a PrintTicket resource.
helpviewer_keywords: ["IXpsOMPrintTicketResource","IXpsOMPrintTicketResource interface [XPS Documents and Packaging]","IXpsOMPrintTicketResource interface [XPS Documents and Packaging]","described","xps.ixpsomprintticketresource","xpsobjectmodel/IXpsOMPrintTicketResource"]
old-location: xps\ixpsomprintticketresource.htm
tech.root: xps
ms.assetid: 2f37dbd2-3078-4aa8-97e7-556a0ff2dd74
ms.date: 12/05/2018
ms.keywords: IXpsOMPrintTicketResource, IXpsOMPrintTicketResource interface [XPS Documents and Packaging], IXpsOMPrintTicketResource interface [XPS Documents and Packaging],described, xps.ixpsomprintticketresource, xpsobjectmodel/IXpsOMPrintTicketResource
f1_keywords:
- xpsobjectmodel/IXpsOMPrintTicketResource
dev_langs:
- c++
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMPrintTicketResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPrintTicketResource interface


## -description


Provides an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to a <b>PrintTicket</b> resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPrintTicketResource</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>. <b>IXpsOMPrintTicketResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPrintTicketResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent">SetContent</a>
</td>
<td align="left" width="63%">
Sets the read-only stream to be  associated with this resource.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createprintticketresource">IXpsOMObjectFactory::CreatePrintTicketResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

