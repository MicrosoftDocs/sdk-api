---
UID: NF:xpsobjectmodel.IXpsOMPartUriCollection.Append
title: IXpsOMPartUriCollection::Append (xpsobjectmodel.h)
description: Appends an IOpcPartUri interface to the end of the collection.
helpviewer_keywords: ["Append","Append method [XPS Documents and Packaging]","Append method [XPS Documents and Packaging]","IXpsOMPartUriCollection interface","IXpsOMPartUriCollection interface [XPS Documents and Packaging]","Append method","IXpsOMPartUriCollection.Append","IXpsOMPartUriCollection::Append","xps.ixpsomparturicollection_append","xpsobjectmodel/IXpsOMPartUriCollection::Append"]
old-location: xps\ixpsomparturicollection_append.htm
tech.root: xps
ms.assetid: 53d450cf-3e31-4d17-99cc-0552df771024
ms.date: 12/05/2018
ms.keywords: Append, Append method [XPS Documents and Packaging], Append method [XPS Documents and Packaging],IXpsOMPartUriCollection interface, IXpsOMPartUriCollection interface [XPS Documents and Packaging],Append method, IXpsOMPartUriCollection.Append, IXpsOMPartUriCollection::Append, xps.ixpsomparturicollection_append, xpsobjectmodel/IXpsOMPartUriCollection::Append
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
 - IXpsOMPartUriCollection::Append
 - xpsobjectmodel/IXpsOMPartUriCollection::Append
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
 - IXpsOMPartUriCollection.Append
---

# IXpsOMPartUriCollection::Append


## -description

Appends an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface to the end of the collection.

## -parameters

### -param partUri [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that is to be appended to the collection.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>