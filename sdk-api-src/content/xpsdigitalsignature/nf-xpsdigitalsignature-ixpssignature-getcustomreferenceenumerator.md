---
UID: NF:xpsdigitalsignature.IXpsSignature.GetCustomReferenceEnumerator
title: IXpsSignature::GetCustomReferenceEnumerator (xpsdigitalsignature.h)
description: Gets a pointer to an IOpcSignatureReferenceEnumerator interface, which enumerates the custom references of the signature.
helpviewer_keywords: ["GetCustomReferenceEnumerator","GetCustomReferenceEnumerator method [XPS Documents and Packaging]","GetCustomReferenceEnumerator method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetCustomReferenceEnumerator method","IXpsSignature.GetCustomReferenceEnumerator","IXpsSignature::GetCustomReferenceEnumerator","xps.ixpssignature_getcustomreferenceenumerator","xpsdigitalsignature/IXpsSignature::GetCustomReferenceEnumerator"]
old-location: xps\ixpssignature_getcustomreferenceenumerator.htm
tech.root: xps
ms.assetid: bcdbd3e0-a19a-448c-92b7-71720eff3386
ms.date: 12/05/2018
ms.keywords: GetCustomReferenceEnumerator, GetCustomReferenceEnumerator method [XPS Documents and Packaging], GetCustomReferenceEnumerator method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetCustomReferenceEnumerator method, IXpsSignature.GetCustomReferenceEnumerator, IXpsSignature::GetCustomReferenceEnumerator, xps.ixpssignature_getcustomreferenceenumerator, xpsdigitalsignature/IXpsSignature::GetCustomReferenceEnumerator
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
 - IXpsSignature::GetCustomReferenceEnumerator
 - xpsdigitalsignature/IXpsSignature::GetCustomReferenceEnumerator
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
 - IXpsSignature.GetCustomReferenceEnumerator
---

# IXpsSignature::GetCustomReferenceEnumerator


## -description

Gets a pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a> interface, which enumerates the custom references of the signature.

## -parameters

### -param customReferenceEnumerator [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a> interface, which enumerates the custom references of the signature.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>