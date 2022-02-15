---
UID: NN:xpsdigitalsignature.IXpsSigningOptions
title: IXpsSigningOptions (xpsdigitalsignature.h)
description: Provides access to the individual signing options that are used by new signatures.
helpviewer_keywords: ["IXpsSigningOptions","IXpsSigningOptions interface [XPS Documents and Packaging]","IXpsSigningOptions interface [XPS Documents and Packaging]","described","xps.ixpssigningoptions","xpsdigitalsignature/IXpsSigningOptions"]
old-location: xps\ixpssigningoptions.htm
tech.root: xps
ms.assetid: 71b9b348-1078-4f55-a071-e5e2f273f85c
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions, IXpsSigningOptions interface [XPS Documents and Packaging], IXpsSigningOptions interface [XPS Documents and Packaging],described, xps.ixpssigningoptions, xpsdigitalsignature/IXpsSigningOptions
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
 - IXpsSigningOptions
 - xpsdigitalsignature/IXpsSigningOptions
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
 - IXpsSigningOptions
---

# IXpsSigningOptions interface


## -description

Provides access to the individual signing options that are used by new signatures.

## -inheritance

The <b>IXpsSigningOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsSigningOptions</b> also has these types of members:

## -remarks

To create a new instance of this interface, call <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">IXpsSignatureManager::CreateSigningOptions</a>.

When a new instance of this interface is returned by <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod  properties are not initialized. These properties  must be initialized before the new interface can be used as a parameter of the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>
