---
UID: NF:xpsobjectmodel.IXpsOMSignatureBlockResourceCollection.GetByPartName
title: IXpsOMSignatureBlockResourceCollection::GetByPartName (xpsobjectmodel.h)
description: Gets an IXpsOMSignatureBlockResource interface pointer from the collection by matching the interface's part name.
helpviewer_keywords: ["GetByPartName","GetByPartName method [XPS Documents and Packaging]","GetByPartName method [XPS Documents and Packaging]","IXpsOMSignatureBlockResourceCollection interface","IXpsOMSignatureBlockResourceCollection interface [XPS Documents and Packaging]","GetByPartName method","IXpsOMSignatureBlockResourceCollection.GetByPartName","IXpsOMSignatureBlockResourceCollection::GetByPartName","xps.ixpsomsignatureblockresourcecollection_getbypartname","xpsobjectmodel/IXpsOMSignatureBlockResourceCollection::GetByPartName"]
old-location: xps\ixpsomsignatureblockresourcecollection_getbypartname.htm
tech.root: xps
ms.assetid: 38e6d6d9-0f31-45e9-8a19-1aae02dfafd3
ms.date: 12/05/2018
ms.keywords: GetByPartName, GetByPartName method [XPS Documents and Packaging], GetByPartName method [XPS Documents and Packaging],IXpsOMSignatureBlockResourceCollection interface, IXpsOMSignatureBlockResourceCollection interface [XPS Documents and Packaging],GetByPartName method, IXpsOMSignatureBlockResourceCollection.GetByPartName, IXpsOMSignatureBlockResourceCollection::GetByPartName, xps.ixpsomsignatureblockresourcecollection_getbypartname, xpsobjectmodel/IXpsOMSignatureBlockResourceCollection::GetByPartName
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
 - IXpsOMSignatureBlockResourceCollection::GetByPartName
 - xpsobjectmodel/IXpsOMSignatureBlockResourceCollection::GetByPartName
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
 - IXpsOMSignatureBlockResourceCollection.GetByPartName
---

# IXpsOMSignatureBlockResourceCollection::GetByPartName


## -description

Gets an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> interface pointer from the collection by matching the interface's part name.

## -parameters

### -param partName [in]

The part name of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> interface to be found in the collection.

### -param signatureBlockResource [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> interface whose part name matches <i>partName</i>. If a matching interface is not found in the collection, a <b>NULL</b> pointer is returned.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection">IXpsOMSignatureBlockResourceCollection</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>