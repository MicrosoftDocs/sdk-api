---
UID: NF:xpsobjectmodel.IXpsOMDashCollection.RemoveAt
title: IXpsOMDashCollection::RemoveAt (xpsobjectmodel.h)
description: Removes and frees an XPS_DASH structure from a specified location in the collection.
helpviewer_keywords: ["IXpsOMDashCollection interface [XPS Documents and Packaging]","RemoveAt method","IXpsOMDashCollection.RemoveAt","IXpsOMDashCollection::RemoveAt","RemoveAt","RemoveAt method [XPS Documents and Packaging]","RemoveAt method [XPS Documents and Packaging]","IXpsOMDashCollection interface","xps.ixpsomdashcollection_removeat","xpsobjectmodel/IXpsOMDashCollection::RemoveAt"]
old-location: xps\ixpsomdashcollection_removeat.htm
tech.root: xps
ms.assetid: 5ccce0d4-c764-4da4-9d7c-463921a92a6a
ms.date: 12/05/2018
ms.keywords: IXpsOMDashCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsOMDashCollection.RemoveAt, IXpsOMDashCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMDashCollection interface, xps.ixpsomdashcollection_removeat, xpsobjectmodel/IXpsOMDashCollection::RemoveAt
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
 - IXpsOMDashCollection::RemoveAt
 - xpsobjectmodel/IXpsOMDashCollection::RemoveAt
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
 - IXpsOMDashCollection.RemoveAt
---

# IXpsOMDashCollection::RemoveAt


## -description

Removes and frees an <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection from which  an <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure is to be removed and freed.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method removes and frees  the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure  referenced by the pointer at  the location specified by <i>index</i>. After freeing the structure, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

The figure that follows illustrates how the collection is changed by the <b>RemoveAt</b> method.

<img alt="A figure that shows how RemoveAt removes an entry from the dash collection" src="./images/dashcollection_removeat.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection">IXpsOMDashCollection</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a>