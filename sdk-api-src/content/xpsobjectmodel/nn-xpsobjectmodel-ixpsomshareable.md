---
UID: NN:xpsobjectmodel.IXpsOMShareable
title: IXpsOMShareable (xpsobjectmodel.h)
description: The base interface for sharable interfaces.
helpviewer_keywords: ["IXpsOMShareable","IXpsOMShareable interface [XPS Documents and Packaging]","IXpsOMShareable interface [XPS Documents and Packaging]","described","xps.ixpsomshareable","xpsobjectmodel/IXpsOMShareable"]
old-location: xps\ixpsomshareable.htm
tech.root: xps
ms.assetid: 2071292f-b898-4ec8-99f7-294c8d820965
ms.date: 12/05/2018
ms.keywords: IXpsOMShareable, IXpsOMShareable interface [XPS Documents and Packaging], IXpsOMShareable interface [XPS Documents and Packaging],described, xps.ixpsomshareable, xpsobjectmodel/IXpsOMShareable
f1_keywords:
- xpsobjectmodel/IXpsOMShareable
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
- IXpsOMShareable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMShareable interface


## -description


The base interface for sharable interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMShareable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMShareable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMShareable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomshareable-getowner">GetOwner</a>
</td>
<td align="left" width="63%">
Gets the <b>IUnknown</b> interface of the parent.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomshareable-gettype">GetType</a>
</td>
<td align="left" width="63%">
Gets the object type of the interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

