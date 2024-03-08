---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigureCollection.Append
title: IXpsOMGeometryFigureCollection::Append (xpsobjectmodel.h)
description: Appends an IXpsOMGeometryFigure interface to the end of the collection.
helpviewer_keywords: ["Append","Append method [XPS Documents and Packaging]","Append method [XPS Documents and Packaging]","IXpsOMGeometryFigureCollection interface","IXpsOMGeometryFigureCollection interface [XPS Documents and Packaging]","Append method","IXpsOMGeometryFigureCollection.Append","IXpsOMGeometryFigureCollection::Append","xps.ixpsomgeometryfigurecollection_append","xpsobjectmodel/IXpsOMGeometryFigureCollection::Append"]
old-location: xps\ixpsomgeometryfigurecollection_append.htm
tech.root: xps
ms.assetid: 9481cd02-74f8-42f6-a347-454dae2aa579
ms.date: 12/05/2018
ms.keywords: Append, Append method [XPS Documents and Packaging], Append method [XPS Documents and Packaging],IXpsOMGeometryFigureCollection interface, IXpsOMGeometryFigureCollection interface [XPS Documents and Packaging],Append method, IXpsOMGeometryFigureCollection.Append, IXpsOMGeometryFigureCollection::Append, xps.ixpsomgeometryfigurecollection_append, xpsobjectmodel/IXpsOMGeometryFigureCollection::Append
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
 - IXpsOMGeometryFigureCollection::Append
 - xpsobjectmodel/IXpsOMGeometryFigureCollection::Append
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
 - IXpsOMGeometryFigureCollection.Append
---

# IXpsOMGeometryFigureCollection::Append


## -description

Appends an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a> interface to the end of the collection.

## -parameters

### -param geometryFigure [in]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a> interface that is to be appended to the collection.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection">IXpsOMGeometryFigureCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>