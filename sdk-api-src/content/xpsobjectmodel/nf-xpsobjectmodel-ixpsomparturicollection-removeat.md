---
UID: NF:xpsobjectmodel.IXpsOMPartUriCollection.RemoveAt
title: IXpsOMPartUriCollection::RemoveAt (xpsobjectmodel.h)
description: Removes and releases an IOpcPartUri interface pointer from a specified location in the collection.
helpviewer_keywords: ["IXpsOMPartUriCollection interface [XPS Documents and Packaging]","RemoveAt method","IXpsOMPartUriCollection.RemoveAt","IXpsOMPartUriCollection::RemoveAt","RemoveAt","RemoveAt method [XPS Documents and Packaging]","RemoveAt method [XPS Documents and Packaging]","IXpsOMPartUriCollection interface","xps.ixpsomparturicollection_removeat","xpsobjectmodel/IXpsOMPartUriCollection::RemoveAt"]
old-location: xps\ixpsomparturicollection_removeat.htm
tech.root: xps
ms.assetid: db5e7595-eba0-454f-8fb3-f129ab537886
ms.date: 12/05/2018
ms.keywords: IXpsOMPartUriCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsOMPartUriCollection.RemoveAt, IXpsOMPartUriCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMPartUriCollection interface, xps.ixpsomparturicollection_removeat, xpsobjectmodel/IXpsOMPartUriCollection::RemoveAt
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
 - IXpsOMPartUriCollection::RemoveAt
 - xpsobjectmodel/IXpsOMPartUriCollection::RemoveAt
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
 - IXpsOMPartUriCollection.RemoveAt
---

# IXpsOMPartUriCollection::RemoveAt


## -description

Removes and releases an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection from which  an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer is to be removed and released.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method releases the interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>