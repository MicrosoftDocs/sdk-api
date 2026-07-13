---
UID: NF:xpsobjectmodel.IXpsOMDictionary.RemoveAt
title: IXpsOMDictionary::RemoveAt (xpsobjectmodel.h)
description: Removes and releases the entry from a specified location in the dictionary.
helpviewer_keywords: ["IXpsOMDictionary interface [XPS Documents and Packaging]","RemoveAt method","IXpsOMDictionary.RemoveAt","IXpsOMDictionary::RemoveAt","RemoveAt","RemoveAt method [XPS Documents and Packaging]","RemoveAt method [XPS Documents and Packaging]","IXpsOMDictionary interface","xps.ixpsomdictionary_removeat","xpsobjectmodel/IXpsOMDictionary::RemoveAt"]
old-location: xps\ixpsomdictionary_removeat.htm
tech.root: xps
ms.assetid: fd86046b-8d87-4093-bfbd-b91e5bacba49
ms.date: 12/05/2018
ms.keywords: IXpsOMDictionary interface [XPS Documents and Packaging],RemoveAt method, IXpsOMDictionary.RemoveAt, IXpsOMDictionary::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMDictionary interface, xps.ixpsomdictionary_removeat, xpsobjectmodel/IXpsOMDictionary::RemoveAt
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
 - IXpsOMDictionary::RemoveAt
 - xpsobjectmodel/IXpsOMDictionary::RemoveAt
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
 - IXpsOMDictionary.RemoveAt
---

# IXpsOMDictionary::RemoveAt


## -description

Removes and releases the entry from a specified location in the dictionary.

## -parameters

### -param index [in]

The zero-based index in the dictionary from which  an entry is to be removed and released.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

At  the location specified by <i>index</i>, this method releases the interface  referenced by the pointer. After releasing the interface, this method compacts the dictionary by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

The figure that follows illustrates how the dictionary is changed by the <b>RemoveAt</b> method.

<img alt="A figure that shows how RemoveAt removes an entry from the dictionary" src="./images/dictionary_removeat.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>