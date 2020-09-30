---
UID: NN:xpsobjectmodel.IXpsOMNameCollection
title: IXpsOMNameCollection (xpsobjectmodel.h)
description: A collection of name strings.
helpviewer_keywords: ["IXpsOMNameCollection","IXpsOMNameCollection interface [XPS Documents and Packaging]","IXpsOMNameCollection interface [XPS Documents and Packaging]","described","xps.ixpsomnamecollection","xpsobjectmodel/IXpsOMNameCollection"]
old-location: xps\ixpsomnamecollection.htm
tech.root: xps
ms.assetid: b27f83fc-0fcf-44e9-a6ce-c3612c5399ff
ms.date: 12/05/2018
ms.keywords: IXpsOMNameCollection, IXpsOMNameCollection interface [XPS Documents and Packaging], IXpsOMNameCollection interface [XPS Documents and Packaging],described, xps.ixpsomnamecollection, xpsobjectmodel/IXpsOMNameCollection
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
 - IXpsOMNameCollection
 - xpsobjectmodel/IXpsOMNameCollection
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
 - IXpsOMNameCollection
---

# IXpsOMNameCollection interface


## -description

A collection of name strings.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMNameCollection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMNameCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMNameCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomnamecollection-getat">GetAt</a>
</td>
<td align="left" width="63%">
Gets the name string that is stored at a specified location in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomnamecollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of name strings in the collection.

</td>
</tr>
</table>

## -remarks

For more information about the collection methods, see <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>