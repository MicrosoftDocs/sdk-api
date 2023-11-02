---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResourceCollection.SetAt
title: IXpsOMRemoteDictionaryResourceCollection::SetAt (xpsobjectmodel.h)
description: Replaces an IXpsOMRemoteDictionaryResource interface pointer at a specified location in the collection.
helpviewer_keywords: ["IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging]","SetAt method","IXpsOMRemoteDictionaryResourceCollection.SetAt","IXpsOMRemoteDictionaryResourceCollection::SetAt","SetAt","SetAt method [XPS Documents and Packaging]","SetAt method [XPS Documents and Packaging]","IXpsOMRemoteDictionaryResourceCollection interface","xps.ixpsomremotedictionaryresourcecollection_setat","xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::SetAt"]
old-location: xps\ixpsomremotedictionaryresourcecollection_setat.htm
tech.root: xps
ms.assetid: 45e33503-dff9-4c59-8d9a-883ff56a30f3
ms.date: 12/05/2018
ms.keywords: IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging],SetAt method, IXpsOMRemoteDictionaryResourceCollection.SetAt, IXpsOMRemoteDictionaryResourceCollection::SetAt, SetAt, SetAt method [XPS Documents and Packaging], SetAt method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResourceCollection interface, xps.ixpsomremotedictionaryresourcecollection_setat, xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::SetAt
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
 - IXpsOMRemoteDictionaryResourceCollection::SetAt
 - xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::SetAt
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
 - IXpsOMRemoteDictionaryResourceCollection.SetAt
---

# IXpsOMRemoteDictionaryResourceCollection::SetAt


## -description

Replaces an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer at a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection where an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer is to be replaced.

### -param object [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer that will replace current contents at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

At the location specified by <i>index</i>, this method releases the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface referenced by the existing pointer, then writes the pointer that is passed in <i>object</i>.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>