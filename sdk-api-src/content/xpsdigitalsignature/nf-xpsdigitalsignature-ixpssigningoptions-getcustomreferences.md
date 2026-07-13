---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetCustomReferences
title: IXpsSigningOptions::GetCustomReferences (xpsdigitalsignature.h)
description: Gets a pointer to an IOpcSignatureReferenceSet interface, which contains a set of signature custom references.
helpviewer_keywords: ["GetCustomReferences","GetCustomReferences method [XPS Documents and Packaging]","GetCustomReferences method [XPS Documents and Packaging]","IXpsSigningOptions interface","IXpsSigningOptions interface [XPS Documents and Packaging]","GetCustomReferences method","IXpsSigningOptions.GetCustomReferences","IXpsSigningOptions::GetCustomReferences","xps.ixpssigningoptions_getcustomreferences","xpsdigitalsignature/IXpsSigningOptions::GetCustomReferences"]
old-location: xps\ixpssigningoptions_getcustomreferences.htm
tech.root: xps
ms.assetid: 1a9ab939-4581-40a9-acd3-2afe02c5e201
ms.date: 12/05/2018
ms.keywords: GetCustomReferences, GetCustomReferences method [XPS Documents and Packaging], GetCustomReferences method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetCustomReferences method, IXpsSigningOptions.GetCustomReferences, IXpsSigningOptions::GetCustomReferences, xps.ixpssigningoptions_getcustomreferences, xpsdigitalsignature/IXpsSigningOptions::GetCustomReferences
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
 - IXpsSigningOptions::GetCustomReferences
 - xpsdigitalsignature/IXpsSigningOptions::GetCustomReferences
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
 - IXpsSigningOptions.GetCustomReferences
---

# IXpsSigningOptions::GetCustomReferences


## -description

Gets a pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface, which contains a set of signature custom references.

## -parameters

### -param customReferenceSet [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface, which contains a set of signature custom references.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The custom reference set that this method returns is empty. To add  a custom reference to this set, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceset-create">Create</a> method of the  interface that is returned in <i>customReferenceSet</i>.

If a custom object must be signed, a reference to  that object  must be added  to the custom object set. For information on adding custom references, refer to  <b>GetCustomReferences</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>