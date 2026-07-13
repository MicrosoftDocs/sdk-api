---
UID: NF:xpsobjectmodel.IXpsOMPartUriCollection.SetAt
title: IXpsOMPartUriCollection::SetAt (xpsobjectmodel.h)
description: Replaces an IOpcPartUri interface pointer at a specified location in the collection.
helpviewer_keywords: ["IXpsOMPartUriCollection interface [XPS Documents and Packaging]","SetAt method","IXpsOMPartUriCollection.SetAt","IXpsOMPartUriCollection::SetAt","SetAt","SetAt method [XPS Documents and Packaging]","SetAt method [XPS Documents and Packaging]","IXpsOMPartUriCollection interface","xps.ixpsomparturicollection_setat","xpsobjectmodel/IXpsOMPartUriCollection::SetAt"]
old-location: xps\ixpsomparturicollection_setat.htm
tech.root: xps
ms.assetid: b41602ae-7d9e-48e4-b9f4-8db09e65f5c8
ms.date: 12/05/2018
ms.keywords: IXpsOMPartUriCollection interface [XPS Documents and Packaging],SetAt method, IXpsOMPartUriCollection.SetAt, IXpsOMPartUriCollection::SetAt, SetAt, SetAt method [XPS Documents and Packaging], SetAt method [XPS Documents and Packaging],IXpsOMPartUriCollection interface, xps.ixpsomparturicollection_setat, xpsobjectmodel/IXpsOMPartUriCollection::SetAt
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
 - IXpsOMPartUriCollection::SetAt
 - xpsobjectmodel/IXpsOMPartUriCollection::SetAt
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
 - IXpsOMPartUriCollection.SetAt
---

# IXpsOMPartUriCollection::SetAt


## -description

Replaces an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer at a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index of the collection where an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer is to be replaced.

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that will replace current contents at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

At the location specified by <i>index</i>, this method releases the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface referenced by the existing pointer, then writes the pointer that is passed in <i>partUri</i>.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>