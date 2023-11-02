---
UID: NF:xpsobjectmodel.IXpsOMDashCollection.InsertAt
title: IXpsOMDashCollection::InsertAt (xpsobjectmodel.h)
description: Inserts an XPS_DASH structure at a specified location in the collection.
helpviewer_keywords: ["IXpsOMDashCollection interface [XPS Documents and Packaging]","InsertAt method","IXpsOMDashCollection.InsertAt","IXpsOMDashCollection::InsertAt","InsertAt","InsertAt method [XPS Documents and Packaging]","InsertAt method [XPS Documents and Packaging]","IXpsOMDashCollection interface","xps.ixpsomdashcollection_insertat","xpsobjectmodel/IXpsOMDashCollection::InsertAt"]
old-location: xps\ixpsomdashcollection_insertat.htm
tech.root: xps
ms.assetid: d9ef0ea9-f427-41ff-b33e-c9b5f49cb7d9
ms.date: 12/05/2018
ms.keywords: IXpsOMDashCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMDashCollection.InsertAt, IXpsOMDashCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMDashCollection interface, xps.ixpsomdashcollection_insertat, xpsobjectmodel/IXpsOMDashCollection::InsertAt
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
 - IXpsOMDashCollection::InsertAt
 - xpsobjectmodel/IXpsOMDashCollection::InsertAt
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
 - IXpsOMDashCollection.InsertAt
---

# IXpsOMDashCollection::InsertAt


## -description

Inserts an <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure at a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection where the structure that is referenced by  <i>dash</i>  is to be inserted.

### -param dash [in]

A pointer to the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure that is to be inserted at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

At the location specified by <i>index</i>, this method inserts the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structure that is passed in <i>dash</i>.  Prior to insertion, the structure in this and all subsequent locations is moved up by one index.

The figure that follows illustrates how the collection is changed by the <b>InsertAt</b> method.

<img alt="A figure that shows how InsertAt adds an entry to the dash collection" src="./images/dashcollection_insertat.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection">IXpsOMDashCollection</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a>