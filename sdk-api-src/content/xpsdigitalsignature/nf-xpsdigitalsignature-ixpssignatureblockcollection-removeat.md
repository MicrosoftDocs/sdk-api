---
UID: NF:xpsdigitalsignature.IXpsSignatureBlockCollection.RemoveAt
title: IXpsSignatureBlockCollection::RemoveAt (xpsdigitalsignature.h)
description: Removes and releases an IXpsSignatureBlock interface pointer from a specified location in the collection.
helpviewer_keywords: ["IXpsSignatureBlockCollection interface [XPS Documents and Packaging]","RemoveAt method","IXpsSignatureBlockCollection.RemoveAt","IXpsSignatureBlockCollection::RemoveAt","RemoveAt","RemoveAt method [XPS Documents and Packaging]","RemoveAt method [XPS Documents and Packaging]","IXpsSignatureBlockCollection interface","xps.ixpssignatureblockcollection_removeat","xpsdigitalsignature/IXpsSignatureBlockCollection::RemoveAt"]
old-location: xps\ixpssignatureblockcollection_removeat.htm
tech.root: xps
ms.assetid: 895f6f0b-6259-4288-90be-659f1ca46d1a
ms.date: 12/05/2018
ms.keywords: IXpsSignatureBlockCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsSignatureBlockCollection.RemoveAt, IXpsSignatureBlockCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsSignatureBlockCollection interface, xps.ixpssignatureblockcollection_removeat, xpsdigitalsignature/IXpsSignatureBlockCollection::RemoveAt
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
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
 - IXpsSignatureBlockCollection::RemoveAt
 - xpsdigitalsignature/IXpsSignatureBlockCollection::RemoveAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureBlockCollection.RemoveAt
---

# IXpsSignatureBlockCollection::RemoveAt


## -description

Removes and releases an <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer from a specified location in the collection.

## -parameters

### -param index

The zero-based index in the collection from which  an <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer is to be removed and released.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

From the location specified by <i>index</i>, this method releases the interface  referenced by an <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> pointer. The method then compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.  For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

Removing a signature block from the collection removes from the package the    SignatureDefinitions part and relationship that correspond to that signature block. This removal breaks existing signatures. In addition, the SignatureDefinitions part name is removed from the list of required XPS parts, which prevents  new signatures from including the removed signature block.

An interface that has been removed from a collection is no longer valid. If an application retains a pointer to the interface and tries to call one of its methods,  the  method will return <b>XPS_E_OBJECT_DETACHED</b>.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection">IXpsSignatureBlockCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>