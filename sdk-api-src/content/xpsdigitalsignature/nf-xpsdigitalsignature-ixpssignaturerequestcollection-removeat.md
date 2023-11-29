---
UID: NF:xpsdigitalsignature.IXpsSignatureRequestCollection.RemoveAt
title: IXpsSignatureRequestCollection::RemoveAt (xpsdigitalsignature.h)
description: Removes and releases an IXpsSignatureRequest interface pointer from a specified location in the collection.
helpviewer_keywords: ["IXpsSignatureRequestCollection interface [XPS Documents and Packaging]","RemoveAt method","IXpsSignatureRequestCollection.RemoveAt","IXpsSignatureRequestCollection::RemoveAt","RemoveAt","RemoveAt method [XPS Documents and Packaging]","RemoveAt method [XPS Documents and Packaging]","IXpsSignatureRequestCollection interface","xps.ixpssignaturerequestcollection_removeat","xpsdigitalsignature/IXpsSignatureRequestCollection::RemoveAt"]
old-location: xps\ixpssignaturerequestcollection_removeat.htm
tech.root: xps
ms.assetid: 6149de80-d0ca-4b6b-a092-b1c30f313df5
ms.date: 12/05/2018
ms.keywords: IXpsSignatureRequestCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsSignatureRequestCollection.RemoveAt, IXpsSignatureRequestCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsSignatureRequestCollection interface, xps.ixpssignaturerequestcollection_removeat, xpsdigitalsignature/IXpsSignatureRequestCollection::RemoveAt
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
 - IXpsSignatureRequestCollection::RemoveAt
 - xpsdigitalsignature/IXpsSignatureRequestCollection::RemoveAt
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
 - IXpsSignatureRequestCollection.RemoveAt
---

# IXpsSignatureRequestCollection::RemoveAt


## -description

Removes and releases an <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a> interface pointer from a specified location in the collection.

## -parameters

### -param index [in]

The zero-based index in the collection from which  an <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a> interface pointer is to be removed and released.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method releases the interface pointer from  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

After the interface has been removed from a collection, it is no longer valid. If an application retains a pointer to the removed interface and tries to call one of the interface's methods,  the  method will return <b>E_UNEXPECTED</b>.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection">IXpsSignatureRequestCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>