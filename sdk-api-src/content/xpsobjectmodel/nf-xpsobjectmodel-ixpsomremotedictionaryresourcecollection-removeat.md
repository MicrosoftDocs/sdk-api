---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResourceCollection.RemoveAt
title: IXpsOMRemoteDictionaryResourceCollection::RemoveAt (xpsobjectmodel.h)
description: Removes and releases an IXpsOMRemoteDictionaryResource interface pointer from a specified location in the collection.
helpviewer_keywords: ["IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging]","RemoveAt method","IXpsOMRemoteDictionaryResourceCollection.RemoveAt","IXpsOMRemoteDictionaryResourceCollection::RemoveAt","RemoveAt","RemoveAt method [XPS Documents and Packaging]","RemoveAt method [XPS Documents and Packaging]","IXpsOMRemoteDictionaryResourceCollection interface","xps.ixpsomremotedictionaryresourcecollection_removeat","xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::RemoveAt"]
old-location: xps\ixpsomremotedictionaryresourcecollection_removeat.htm
tech.root: xps
ms.assetid: a144a3b4-3935-4377-b97d-3d3a723ea3b7
ms.date: 12/05/2018
ms.keywords: IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsOMRemoteDictionaryResourceCollection.RemoveAt, IXpsOMRemoteDictionaryResourceCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResourceCollection interface, xps.ixpsomremotedictionaryresourcecollection_removeat, xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::RemoveAt
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
 - IXpsOMRemoteDictionaryResourceCollection::RemoveAt
 - xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::RemoveAt
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
 - IXpsOMRemoteDictionaryResourceCollection.RemoveAt
---

# IXpsOMRemoteDictionaryResourceCollection::RemoveAt


## -description

Removes and releases an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection from which  an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer is to be removed and released.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method releases the interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>