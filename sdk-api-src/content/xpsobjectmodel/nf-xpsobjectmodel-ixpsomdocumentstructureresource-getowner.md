---
UID: NF:xpsobjectmodel.IXpsOMDocumentStructureResource.GetOwner
title: IXpsOMDocumentStructureResource::GetOwner (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMDocument interface that contains the resource. (IXpsOMDocumentStructureResource.GetOwner)
helpviewer_keywords: ["GetOwner","GetOwner method [XPS Documents and Packaging]","GetOwner method [XPS Documents and Packaging]","IXpsOMDocumentStructureResource interface","IXpsOMDocumentStructureResource interface [XPS Documents and Packaging]","GetOwner method","IXpsOMDocumentStructureResource.GetOwner","IXpsOMDocumentStructureResource::GetOwner","xps.ixpsomdocumentstructureresource_getowner","xpsobjectmodel/IXpsOMDocumentStructureResource::GetOwner"]
old-location: xps\ixpsomdocumentstructureresource_getowner.htm
tech.root: xps
ms.assetid: cbaedef0-f1a9-4c2c-88ae-1542cfbff252
ms.date: 12/05/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMDocumentStructureResource interface, IXpsOMDocumentStructureResource interface [XPS Documents and Packaging],GetOwner method, IXpsOMDocumentStructureResource.GetOwner, IXpsOMDocumentStructureResource::GetOwner, xps.ixpsomdocumentstructureresource_getowner, xpsobjectmodel/IXpsOMDocumentStructureResource::GetOwner
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
 - IXpsOMDocumentStructureResource::GetOwner
 - xpsobjectmodel/IXpsOMDocumentStructureResource::GetOwner
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
 - IXpsOMDocumentStructureResource.GetOwner
---

# IXpsOMDocumentStructureResource::GetOwner


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface that contains the resource.

## -parameters

### -param owner [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface that contains the resource. If the resource is not part of a document, a <b>NULL</b> pointer is returned.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
