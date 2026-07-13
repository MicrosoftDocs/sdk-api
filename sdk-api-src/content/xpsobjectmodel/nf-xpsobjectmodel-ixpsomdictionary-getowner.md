---
UID: NF:xpsobjectmodel.IXpsOMDictionary.GetOwner
title: IXpsOMDictionary::GetOwner (xpsobjectmodel.h)
description: Gets a pointer to the interface that contains the dictionary.
helpviewer_keywords: ["GetOwner","GetOwner method [XPS Documents and Packaging]","GetOwner method [XPS Documents and Packaging]","IXpsOMDictionary interface","IXpsOMDictionary interface [XPS Documents and Packaging]","GetOwner method","IXpsOMDictionary.GetOwner","IXpsOMDictionary::GetOwner","xps.ixpsomdictionary_getowner","xpsobjectmodel/IXpsOMDictionary::GetOwner"]
old-location: xps\ixpsomdictionary_getowner.htm
tech.root: xps
ms.assetid: 3570ad03-2b68-4294-b236-86bd372876a2
ms.date: 12/05/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMDictionary interface, IXpsOMDictionary interface [XPS Documents and Packaging],GetOwner method, IXpsOMDictionary.GetOwner, IXpsOMDictionary::GetOwner, xps.ixpsomdictionary_getowner, xpsobjectmodel/IXpsOMDictionary::GetOwner
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
 - IXpsOMDictionary::GetOwner
 - xpsobjectmodel/IXpsOMDictionary::GetOwner
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
 - IXpsOMDictionary.GetOwner
---

# IXpsOMDictionary::GetOwner


## -description

Gets a pointer to the interface that contains the dictionary.

## -parameters

### -param owner [out, retval]

The <b>IUnknown</b> interface of the interface that contains the dictionary.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>