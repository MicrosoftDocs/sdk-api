---
UID: NN:xpsdigitalsignature.IXpsSignatureRequest
title: IXpsSignatureRequest (xpsdigitalsignature.h)
description: Accesses the components of a signature request.
helpviewer_keywords: ["IXpsSignatureRequest","IXpsSignatureRequest interface [XPS Documents and Packaging]","IXpsSignatureRequest interface [XPS Documents and Packaging]","described","xps.ixpssignaturerequest","xpsdigitalsignature/IXpsSignatureRequest"]
old-location: xps\ixpssignaturerequest.htm
tech.root: xps
ms.assetid: 5ece2402-ab0e-4695-b9d7-478a65199ec8
ms.date: 12/05/2018
ms.keywords: IXpsSignatureRequest, IXpsSignatureRequest interface [XPS Documents and Packaging], IXpsSignatureRequest interface [XPS Documents and Packaging],described, xps.ixpssignaturerequest, xpsdigitalsignature/IXpsSignatureRequest
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
 - IXpsSignatureRequest
 - xpsdigitalsignature/IXpsSignatureRequest
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
 - IXpsSignatureRequest
---

# IXpsSignatureRequest interface


## -description

Accesses the components of a signature request.

## -inheritance

The <b>IXpsSignatureRequest</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsSignatureRequest</b> also has these types of members:

## -remarks

The <b>IXpsSignatureRequest</b> interface corresponds to a single <b>SignatureDefinition</b> element in the markup of the SignatureDefinitons part.

This <b>SignatureDefinition</b> element markup is described in section 10.2.2 of the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>. 

All signature requests are 
stored in a request collection of a signature block. They cannot exist independently from the <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface from which they were instantiated.

## -see-also

<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>
