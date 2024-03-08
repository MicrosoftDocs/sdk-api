---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetSignatureId
title: IXpsSigningOptions::SetSignatureId (xpsdigitalsignature.h)
description: Sets the value of the Id attribute of the Signature element. (IXpsSigningOptions.SetSignatureId)
helpviewer_keywords: ["IXpsSigningOptions interface [XPS Documents and Packaging]","SetSignatureId method","IXpsSigningOptions.SetSignatureId","IXpsSigningOptions::SetSignatureId","SetSignatureId","SetSignatureId method [XPS Documents and Packaging]","SetSignatureId method [XPS Documents and Packaging]","IXpsSigningOptions interface","xps.ixpssigningoptions_setsignatureid","xpsdigitalsignature/IXpsSigningOptions::SetSignatureId"]
old-location: xps\ixpssigningoptions_setsignatureid.htm
tech.root: xps
ms.assetid: 314199f2-15bc-4ede-b18c-96c1dbfe5367
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetSignatureId method, IXpsSigningOptions.SetSignatureId, IXpsSigningOptions::SetSignatureId, SetSignatureId, SetSignatureId method [XPS Documents and Packaging], SetSignatureId method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setsignatureid, xpsdigitalsignature/IXpsSigningOptions::SetSignatureId
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
 - IXpsSigningOptions::SetSignatureId
 - xpsdigitalsignature/IXpsSigningOptions::SetSignatureId
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
 - IXpsSigningOptions.SetSignatureId
---

# IXpsSigningOptions::SetSignatureId


## -description

Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.

## -parameters

### -param signatureId [in]

The string value to be set as the <b>Id</b> attribute of the <b>Signature</b> element.  If this parameter is <b>NULL</b>, the <b>Id</b> attribute is cleared.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
