---
UID: NF:xpsobjectmodel.IXpsOMStoryFragmentsResource.GetOwner
title: IXpsOMStoryFragmentsResource::GetOwner (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMPage interface that contains this resource.
helpviewer_keywords: ["GetOwner","GetOwner method [XPS Documents and Packaging]","GetOwner method [XPS Documents and Packaging]","IXpsOMStoryFragmentsResource interface","IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging]","GetOwner method","IXpsOMStoryFragmentsResource.GetOwner","IXpsOMStoryFragmentsResource::GetOwner","xps.ixpsomstoryfragmentsresource_getowner","xpsobjectmodel/IXpsOMStoryFragmentsResource::GetOwner"]
old-location: xps\ixpsomstoryfragmentsresource_getowner.htm
tech.root: xps
ms.assetid: 8dc44277-d296-4747-8dd7-8901a94b5213
ms.date: 12/05/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMStoryFragmentsResource interface, IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging],GetOwner method, IXpsOMStoryFragmentsResource.GetOwner, IXpsOMStoryFragmentsResource::GetOwner, xps.ixpsomstoryfragmentsresource_getowner, xpsobjectmodel/IXpsOMStoryFragmentsResource::GetOwner
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
 - IXpsOMStoryFragmentsResource::GetOwner
 - xpsobjectmodel/IXpsOMStoryFragmentsResource::GetOwner
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
 - IXpsOMStoryFragmentsResource.GetOwner
---

# IXpsOMStoryFragmentsResource::GetOwner


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface that contains this resource.

## -parameters

### -param owner [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface that contains this resource. If the resource is not part of a page, a <b>NULL</b> pointer is returned.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>