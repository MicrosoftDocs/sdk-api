---
UID: NF:xpsobjectmodel.IXpsOMVisualCollection.InsertAt
title: IXpsOMVisualCollection::InsertAt (xpsobjectmodel.h)
description: Inserts an IXpsOMVisual interface pointer at a specified location in the collection.
helpviewer_keywords: ["IXpsOMVisualCollection interface [XPS Documents and Packaging]","InsertAt method","IXpsOMVisualCollection.InsertAt","IXpsOMVisualCollection::InsertAt","InsertAt","InsertAt method [XPS Documents and Packaging]","InsertAt method [XPS Documents and Packaging]","IXpsOMVisualCollection interface","xps.ixpsomvisualcollection_insertat","xpsobjectmodel/IXpsOMVisualCollection::InsertAt"]
old-location: xps\ixpsomvisualcollection_insertat.htm
tech.root: xps
ms.assetid: b4becd2b-c5f4-4d4d-a142-9f4fe11fafd3
ms.date: 12/05/2018
ms.keywords: IXpsOMVisualCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMVisualCollection.InsertAt, IXpsOMVisualCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMVisualCollection interface, xps.ixpsomvisualcollection_insertat, xpsobjectmodel/IXpsOMVisualCollection::InsertAt
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
 - IXpsOMVisualCollection::InsertAt
 - xpsobjectmodel/IXpsOMVisualCollection::InsertAt
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
 - IXpsOMVisualCollection.InsertAt
---

# IXpsOMVisualCollection::InsertAt


## -description

Inserts an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointer at a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index of the collection where the interface pointer that is passed in <i>object</i>  is to be inserted.

### -param object [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointer that is to be inserted at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

At the location specified by <i>index</i>, this method inserts the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a> interface pointer that is passed in <i>object</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection">IXpsOMVisualCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>