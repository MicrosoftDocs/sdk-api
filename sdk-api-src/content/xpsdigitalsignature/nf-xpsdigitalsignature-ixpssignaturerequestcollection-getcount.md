---
UID: NF:xpsdigitalsignature.IXpsSignatureRequestCollection.GetCount
title: IXpsSignatureRequestCollection::GetCount (xpsdigitalsignature.h)
description: Gets the number of IXpsSignatureRequest interface pointers in the collection.
helpviewer_keywords: ["GetCount","GetCount method [XPS Documents and Packaging]","GetCount method [XPS Documents and Packaging]","IXpsSignatureRequestCollection interface","IXpsSignatureRequestCollection interface [XPS Documents and Packaging]","GetCount method","IXpsSignatureRequestCollection.GetCount","IXpsSignatureRequestCollection::GetCount","xps.ixpssignaturerequestcollection_getcount","xpsdigitalsignature/IXpsSignatureRequestCollection::GetCount"]
old-location: xps\ixpssignaturerequestcollection_getcount.htm
tech.root: xps
ms.assetid: e85d776e-6e26-46fa-bcaa-d99737ec1211
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [XPS Documents and Packaging], GetCount method [XPS Documents and Packaging],IXpsSignatureRequestCollection interface, IXpsSignatureRequestCollection interface [XPS Documents and Packaging],GetCount method, IXpsSignatureRequestCollection.GetCount, IXpsSignatureRequestCollection::GetCount, xps.ixpssignaturerequestcollection_getcount, xpsdigitalsignature/IXpsSignatureRequestCollection::GetCount
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
 - IXpsSignatureRequestCollection::GetCount
 - xpsdigitalsignature/IXpsSignatureRequestCollection::GetCount
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
 - IXpsSignatureRequestCollection.GetCount
---

# IXpsSignatureRequestCollection::GetCount


## -description

Gets the number of <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a> interface pointers in the collection.

## -parameters

### -param count [out, retval]

The number of <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a> interface pointers in the collection.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection">IXpsSignatureRequestCollection</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>