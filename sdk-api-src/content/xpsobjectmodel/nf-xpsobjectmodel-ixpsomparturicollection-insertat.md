---
UID: NF:xpsobjectmodel.IXpsOMPartUriCollection.InsertAt
title: IXpsOMPartUriCollection::InsertAt (xpsobjectmodel.h)
description: Inserts an IOpcPartUri interface pointer at a specified location in the collection.
helpviewer_keywords: ["IXpsOMPartUriCollection interface [XPS Documents and Packaging]","InsertAt method","IXpsOMPartUriCollection.InsertAt","IXpsOMPartUriCollection::InsertAt","InsertAt","InsertAt method [XPS Documents and Packaging]","InsertAt method [XPS Documents and Packaging]","IXpsOMPartUriCollection interface","xps.ixpsomparturicollection_insertat","xpsobjectmodel/IXpsOMPartUriCollection::InsertAt"]
old-location: xps\ixpsomparturicollection_insertat.htm
tech.root: xps
ms.assetid: 672e3cc7-ac25-4d9d-9983-66cf6d26f574
ms.date: 12/05/2018
ms.keywords: IXpsOMPartUriCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMPartUriCollection.InsertAt, IXpsOMPartUriCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMPartUriCollection interface, xps.ixpsomparturicollection_insertat, xpsobjectmodel/IXpsOMPartUriCollection::InsertAt
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
 - IXpsOMPartUriCollection::InsertAt
 - xpsobjectmodel/IXpsOMPartUriCollection::InsertAt
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
 - IXpsOMPartUriCollection.InsertAt
---

# IXpsOMPartUriCollection::InsertAt


## -description

Inserts an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer at a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index of the collection where the interface pointer that is passed in <i>partUri</i> is to be inserted.

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that is to be inserted at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

At the location specified by <i>index</i>, this method inserts the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that is passed in <i>partUri</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>