---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetSignatureId
title: IXpsSigningOptions::GetSignatureId (xpsdigitalsignature.h)
description: Gets the value of the Id attribute of the Signature element. (IXpsSigningOptions.GetSignatureId)
helpviewer_keywords: ["GetSignatureId","GetSignatureId method [XPS Documents and Packaging]","GetSignatureId method [XPS Documents and Packaging]","IXpsSigningOptions interface","IXpsSigningOptions interface [XPS Documents and Packaging]","GetSignatureId method","IXpsSigningOptions.GetSignatureId","IXpsSigningOptions::GetSignatureId","xps.ixpssigningoptions_getsignatureid","xpsdigitalsignature/IXpsSigningOptions::GetSignatureId"]
old-location: xps\ixpssigningoptions_getsignatureid.htm
tech.root: xps
ms.assetid: ebcb9f75-c9da-4559-9a9f-915b166801bf
ms.date: 12/05/2018
ms.keywords: GetSignatureId, GetSignatureId method [XPS Documents and Packaging], GetSignatureId method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetSignatureId method, IXpsSigningOptions.GetSignatureId, IXpsSigningOptions::GetSignatureId, xps.ixpssigningoptions_getsignatureid, xpsdigitalsignature/IXpsSigningOptions::GetSignatureId
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
 - IXpsSigningOptions::GetSignatureId
 - xpsdigitalsignature/IXpsSigningOptions::GetSignatureId
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
 - IXpsSigningOptions.GetSignatureId
---

# IXpsSigningOptions::GetSignatureId


## -description

Gets the value of the <b>Id</b> attribute of the <b>Signature</b> element.

## -parameters

### -param signatureId [out, retval]

The value of the <b>Id</b> attribute of the <b>Signature</b> element. If  the <b>Id</b> attribute is not present, the method returns an empty string.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method allocates the memory used by the string that is returned in <i>signatureId</i>.  If <i>signatureId</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

The default value of the signature ID is an empty string.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
