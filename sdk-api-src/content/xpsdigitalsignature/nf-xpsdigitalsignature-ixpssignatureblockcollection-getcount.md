---
UID: NF:xpsdigitalsignature.IXpsSignatureBlockCollection.GetCount
title: IXpsSignatureBlockCollection::GetCount (xpsdigitalsignature.h)
description: Gets the number of IXpsSignatureBlock interface pointers in the collection.
helpviewer_keywords: ["GetCount","GetCount method [XPS Documents and Packaging]","GetCount method [XPS Documents and Packaging]","IXpsSignatureBlockCollection interface","IXpsSignatureBlockCollection interface [XPS Documents and Packaging]","GetCount method","IXpsSignatureBlockCollection.GetCount","IXpsSignatureBlockCollection::GetCount","xps.ixpssignatureblockcollection_getcount","xpsdigitalsignature/IXpsSignatureBlockCollection::GetCount"]
old-location: xps\ixpssignatureblockcollection_getcount.htm
tech.root: xps
ms.assetid: d748e974-7350-44cd-9599-111f402d20e2
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [XPS Documents and Packaging], GetCount method [XPS Documents and Packaging],IXpsSignatureBlockCollection interface, IXpsSignatureBlockCollection interface [XPS Documents and Packaging],GetCount method, IXpsSignatureBlockCollection.GetCount, IXpsSignatureBlockCollection::GetCount, xps.ixpssignatureblockcollection_getcount, xpsdigitalsignature/IXpsSignatureBlockCollection::GetCount
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
 - IXpsSignatureBlockCollection::GetCount
 - xpsdigitalsignature/IXpsSignatureBlockCollection::GetCount
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
 - IXpsSignatureBlockCollection.GetCount
---

# IXpsSignatureBlockCollection::GetCount


## -description

Gets the number of <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointers in the collection.

## -parameters

### -param count [out, retval]

The number of <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointers in the collection.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection">IXpsSignatureBlockCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>