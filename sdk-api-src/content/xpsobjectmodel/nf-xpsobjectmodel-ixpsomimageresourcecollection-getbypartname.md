---
UID: NF:xpsobjectmodel.IXpsOMImageResourceCollection.GetByPartName
title: IXpsOMImageResourceCollection::GetByPartName (xpsobjectmodel.h)
description: Gets an IXpsOMImageResource interface pointer from the collection by matching the interface's part name.
helpviewer_keywords: ["GetByPartName","GetByPartName method [XPS Documents and Packaging]","GetByPartName method [XPS Documents and Packaging]","IXpsOMImageResourceCollection interface","IXpsOMImageResourceCollection interface [XPS Documents and Packaging]","GetByPartName method","IXpsOMImageResourceCollection.GetByPartName","IXpsOMImageResourceCollection::GetByPartName","xps.ixpsomimageresourcecollection_getbypartname","xpsobjectmodel/IXpsOMImageResourceCollection::GetByPartName"]
old-location: xps\ixpsomimageresourcecollection_getbypartname.htm
tech.root: xps
ms.assetid: 559461b4-49c1-4dd9-a370-05bfc71b4f36
ms.date: 12/05/2018
ms.keywords: GetByPartName, GetByPartName method [XPS Documents and Packaging], GetByPartName method [XPS Documents and Packaging],IXpsOMImageResourceCollection interface, IXpsOMImageResourceCollection interface [XPS Documents and Packaging],GetByPartName method, IXpsOMImageResourceCollection.GetByPartName, IXpsOMImageResourceCollection::GetByPartName, xps.ixpsomimageresourcecollection_getbypartname, xpsobjectmodel/IXpsOMImageResourceCollection::GetByPartName
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
 - IXpsOMImageResourceCollection::GetByPartName
 - xpsobjectmodel/IXpsOMImageResourceCollection::GetByPartName
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
 - IXpsOMImageResourceCollection.GetByPartName
---

# IXpsOMImageResourceCollection::GetByPartName


## -description

Gets an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface pointer from the collection by matching the interface's part name.

## -parameters

### -param partName [in]

The part name of the interface that is to be found in the collection.

### -param part [out, retval]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface whose part name matches <i>partName</i>.  If a matching interface is not found in the collection, a <b>NULL</b> pointer is returned.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection">IXpsOMImageResourceCollection</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>