---
UID: NN:xpsdigitalsignature.IXpsSignature
title: IXpsSignature (xpsdigitalsignature.h)
description: Represents a single digital signature.
helpviewer_keywords: ["IXpsSignature","IXpsSignature interface [XPS Documents and Packaging]","IXpsSignature interface [XPS Documents and Packaging]","described","xps.ixpssignature","xpsdigitalsignature/IXpsSignature"]
old-location: xps\ixpssignature.htm
tech.root: xps
ms.assetid: 23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5
ms.date: 12/05/2018
ms.keywords: IXpsSignature, IXpsSignature interface [XPS Documents and Packaging], IXpsSignature interface [XPS Documents and Packaging],described, xps.ixpssignature, xpsdigitalsignature/IXpsSignature
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
 - IXpsSignature
 - xpsdigitalsignature/IXpsSignature
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
 - IXpsSignature
---

# IXpsSignature interface


## -description

Represents a single digital signature.

## -inheritance

The <b>IXpsSignature</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsSignature</b> also has these types of members:

## -remarks

This interface is linked to the signature manager from which it was instantiated and it cannot exist independently.

An <b>IXpsSignature</b> interface may represent a signature that is not XPS compliant. For example, it could represent a signature that includes only custom parts, which is not allowed by the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>



<a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a>
