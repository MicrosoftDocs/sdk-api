---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigureCollection.RemoveAt
title: IXpsOMGeometryFigureCollection::RemoveAt (xpsobjectmodel.h)
description: Removes and releases an IXpsOMGeometryFigure interface pointer from a specified location in the collection.
helpviewer_keywords: ["IXpsOMGeometryFigureCollection interface [XPS Documents and Packaging]","RemoveAt method","IXpsOMGeometryFigureCollection.RemoveAt","IXpsOMGeometryFigureCollection::RemoveAt","RemoveAt","RemoveAt method [XPS Documents and Packaging]","RemoveAt method [XPS Documents and Packaging]","IXpsOMGeometryFigureCollection interface","xps.ixpsomgeometryfigurecollection_removeat","xpsobjectmodel/IXpsOMGeometryFigureCollection::RemoveAt"]
old-location: xps\ixpsomgeometryfigurecollection_removeat.htm
tech.root: xps
ms.assetid: f3030eea-e87f-4bb8-9835-e6bc052ff0ef
ms.date: 12/05/2018
ms.keywords: IXpsOMGeometryFigureCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsOMGeometryFigureCollection.RemoveAt, IXpsOMGeometryFigureCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMGeometryFigureCollection interface, xps.ixpsomgeometryfigurecollection_removeat, xpsobjectmodel/IXpsOMGeometryFigureCollection::RemoveAt
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
 - IXpsOMGeometryFigureCollection::RemoveAt
 - xpsobjectmodel/IXpsOMGeometryFigureCollection::RemoveAt
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
 - IXpsOMGeometryFigureCollection.RemoveAt
---

# IXpsOMGeometryFigureCollection::RemoveAt


## -description

Removes and releases an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a> interface pointer from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection from which  an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a> interface pointer is to be removed and released.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method releases the interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection">IXpsOMGeometryFigureCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>