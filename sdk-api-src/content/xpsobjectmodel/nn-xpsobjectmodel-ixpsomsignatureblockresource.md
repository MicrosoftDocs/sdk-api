---
UID: NN:xpsobjectmodel.IXpsOMSignatureBlockResource
title: IXpsOMSignatureBlockResource (xpsobjectmodel.h)
description: Provides an IStream interface to a signature block resource.
helpviewer_keywords: ["IXpsOMSignatureBlockResource","IXpsOMSignatureBlockResource interface [XPS Documents and Packaging]","IXpsOMSignatureBlockResource interface [XPS Documents and Packaging]","described","xps.ixpsomsignatureblockresource","xpsobjectmodel/IXpsOMSignatureBlockResource"]
old-location: xps\ixpsomsignatureblockresource.htm
tech.root: xps
ms.assetid: f5052470-487d-4f47-8d42-70538a4a45a8
ms.date: 12/05/2018
ms.keywords: IXpsOMSignatureBlockResource, IXpsOMSignatureBlockResource interface [XPS Documents and Packaging], IXpsOMSignatureBlockResource interface [XPS Documents and Packaging],described, xps.ixpsomsignatureblockresource, xpsobjectmodel/IXpsOMSignatureBlockResource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMSignatureBlockResource
 - xpsobjectmodel/IXpsOMSignatureBlockResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMSignatureBlockResource
---

# IXpsOMSignatureBlockResource interface


## -description

Provides an IStream interface to a signature block resource.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMSignatureBlockResource</b> interface inherits from <a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>. <b>IXpsOMSignatureBlockResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMSignatureBlockResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomsignatureblockresource-getowner">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface that contains the resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomsignatureblockresource-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomsignatureblockresource-setcontent">SetContent</a>
</td>
<td align="left" width="63%">
Sets the read-only stream to be associated with this resource.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createsignatureblockresource">IXpsOMObjectFactory::CreateSignatureBlockResource</a>



<a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>