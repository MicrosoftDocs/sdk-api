---
UID: NF:xpsobjectmodel.IXpsOMFontResourceCollection.GetByPartName
title: IXpsOMFontResourceCollection::GetByPartName (xpsobjectmodel.h)
description: Gets an IXpsOMFontResource interface pointer from the collection by matching the interface's part name.
helpviewer_keywords: ["GetByPartName","GetByPartName method [XPS Documents and Packaging]","GetByPartName method [XPS Documents and Packaging]","IXpsOMFontResourceCollection interface","IXpsOMFontResourceCollection interface [XPS Documents and Packaging]","GetByPartName method","IXpsOMFontResourceCollection.GetByPartName","IXpsOMFontResourceCollection::GetByPartName","xps.ixpsomfontresourcecollection_getbypartname","xpsobjectmodel/IXpsOMFontResourceCollection::GetByPartName"]
old-location: xps\ixpsomfontresourcecollection_getbypartname.htm
tech.root: xps
ms.assetid: f40830ec-e77b-4c47-9041-b0df5becf9fa
ms.date: 12/05/2018
ms.keywords: GetByPartName, GetByPartName method [XPS Documents and Packaging], GetByPartName method [XPS Documents and Packaging],IXpsOMFontResourceCollection interface, IXpsOMFontResourceCollection interface [XPS Documents and Packaging],GetByPartName method, IXpsOMFontResourceCollection.GetByPartName, IXpsOMFontResourceCollection::GetByPartName, xps.ixpsomfontresourcecollection_getbypartname, xpsobjectmodel/IXpsOMFontResourceCollection::GetByPartName
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
 - IXpsOMFontResourceCollection::GetByPartName
 - xpsobjectmodel/IXpsOMFontResourceCollection::GetByPartName
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
 - IXpsOMFontResourceCollection.GetByPartName
---

# IXpsOMFontResourceCollection::GetByPartName


## -description

Gets an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface pointer from the collection by matching the interface's part name.

## -parameters

### -param partName [in]

The part name of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface to be found in the collection.

### -param part [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface that has the matching part name. If a matching interface is not found in the collection, a <b>NULL</b> pointer is returned.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection">IXpsOMFontResourceCollection</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>