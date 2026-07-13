---
UID: NF:xpsobjectmodel.IXpsOMSignatureBlockResourceCollection.InsertAt
title: IXpsOMSignatureBlockResourceCollection::InsertAt (xpsobjectmodel.h)
description: Inserts an IXpsOMSignatureBlockResource interface pointer at a specified location in the collection.
helpviewer_keywords: ["IXpsOMSignatureBlockResourceCollection interface [XPS Documents and Packaging]","InsertAt method","IXpsOMSignatureBlockResourceCollection.InsertAt","IXpsOMSignatureBlockResourceCollection::InsertAt","InsertAt","InsertAt method [XPS Documents and Packaging]","InsertAt method [XPS Documents and Packaging]","IXpsOMSignatureBlockResourceCollection interface","xps.ixpsomsignatureblockresourcecollection_insertat","xpsobjectmodel/IXpsOMSignatureBlockResourceCollection::InsertAt"]
old-location: xps\ixpsomsignatureblockresourcecollection_insertat.htm
tech.root: xps
ms.assetid: bcb9d712-35b6-4dfc-91dc-dd376950e1e8
ms.date: 12/05/2018
ms.keywords: IXpsOMSignatureBlockResourceCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMSignatureBlockResourceCollection.InsertAt, IXpsOMSignatureBlockResourceCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMSignatureBlockResourceCollection interface, xps.ixpsomsignatureblockresourcecollection_insertat, xpsobjectmodel/IXpsOMSignatureBlockResourceCollection::InsertAt
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
 - IXpsOMSignatureBlockResourceCollection::InsertAt
 - xpsobjectmodel/IXpsOMSignatureBlockResourceCollection::InsertAt
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
 - IXpsOMSignatureBlockResourceCollection.InsertAt
---

# IXpsOMSignatureBlockResourceCollection::InsertAt


## -description

Inserts an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> interface pointer at a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection where the interface pointer that is passed in <i>signatureBlockResource</i>  is to be inserted.

### -param signatureBlockResource [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> interface pointer that is to be inserted at the location specified by <i>index</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

At the location specified by <i>index</i>, this method inserts the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> interface pointer that is passed in <i>signatureBlockResource</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection">IXpsOMSignatureBlockResourceCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>