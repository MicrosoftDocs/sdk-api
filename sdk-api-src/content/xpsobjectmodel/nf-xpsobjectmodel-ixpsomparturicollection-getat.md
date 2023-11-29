---
UID: NF:xpsobjectmodel.IXpsOMPartUriCollection.GetAt
title: IXpsOMPartUriCollection::GetAt (xpsobjectmodel.h)
description: Gets an IOpcPartUri interface pointer from a specified location in the collection.
helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsOMPartUriCollection interface","IXpsOMPartUriCollection interface [XPS Documents and Packaging]","GetAt method","IXpsOMPartUriCollection.GetAt","IXpsOMPartUriCollection::GetAt","xps.ixpsomparturicollection_getat","xpsobjectmodel/IXpsOMPartUriCollection::GetAt"]
old-location: xps\ixpsomparturicollection_getat.htm
tech.root: xps
ms.assetid: 9d7fcc13-13f5-494d-b6b2-d1180902ec08
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMPartUriCollection interface, IXpsOMPartUriCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMPartUriCollection.GetAt, IXpsOMPartUriCollection::GetAt, xps.ixpsomparturicollection_getat, xpsobjectmodel/IXpsOMPartUriCollection::GetAt
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
 - IXpsOMPartUriCollection::GetAt
 - xpsobjectmodel/IXpsOMPartUriCollection::GetAt
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
 - IXpsOMPartUriCollection.GetAt
---

# IXpsOMPartUriCollection::GetAt


## -description

Gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer to be obtained.

### -param partUri [out, retval]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>