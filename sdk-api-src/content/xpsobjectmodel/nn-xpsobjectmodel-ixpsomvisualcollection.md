---
UID: NN:xpsobjectmodel.IXpsOMVisualCollection
title: IXpsOMVisualCollection (xpsobjectmodel.h)
description: A collection of IXpsOMVisual interface pointers.
helpviewer_keywords: ["IXpsOMVisualCollection","IXpsOMVisualCollection interface [XPS Documents and Packaging]","IXpsOMVisualCollection interface [XPS Documents and Packaging]","described","xps.ixpsomvisualcollection","xpsobjectmodel/IXpsOMVisualCollection"]
old-location: xps\ixpsomvisualcollection.htm
tech.root: xps
ms.assetid: f373b437-3973-40aa-9cac-a6b196a3e5d1
ms.date: 12/05/2018
ms.keywords: IXpsOMVisualCollection, IXpsOMVisualCollection interface [XPS Documents and Packaging], IXpsOMVisualCollection interface [XPS Documents and Packaging],described, xps.ixpsomvisualcollection, xpsobjectmodel/IXpsOMVisualCollection
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
 - IXpsOMVisualCollection
 - xpsobjectmodel/IXpsOMVisualCollection
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
 - IXpsOMVisualCollection
---

# IXpsOMVisualCollection interface


## -description

A collection of <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointers.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMVisualCollection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMVisualCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMVisualCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualcollection-append">Append</a>
</td>
<td align="left" width="63%">
Appends an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface to the end of the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualcollection-getat">GetAt</a>
</td>
<td align="left" width="63%">
Gets an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualcollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointers in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualcollection-insertat">InsertAt</a>
</td>
<td align="left" width="63%">
Inserts an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointer at a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualcollection-removeat">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes and releases an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualcollection-setat">SetAt</a>
</td>
<td align="left" width="63%">
Replaces an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointer at a specified location in the collection.
            

</td>
</tr>
</table>

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>