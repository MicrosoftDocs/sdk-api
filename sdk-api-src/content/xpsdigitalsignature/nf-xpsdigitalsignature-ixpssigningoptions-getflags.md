---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetFlags
title: IXpsSigningOptions::GetFlags (xpsdigitalsignature.h)
description: Gets the XPS_SIGN_FLAGS value that specifies the signing flags to be used for this signature.
helpviewer_keywords: ["GetFlags","GetFlags method [XPS Documents and Packaging]","GetFlags method [XPS Documents and Packaging]","IXpsSigningOptions interface","IXpsSigningOptions interface [XPS Documents and Packaging]","GetFlags method","IXpsSigningOptions.GetFlags","IXpsSigningOptions::GetFlags","xps.ixpssigningoptions_getflags","xpsdigitalsignature/IXpsSigningOptions::GetFlags"]
old-location: xps\ixpssigningoptions_getflags.htm
tech.root: xps
ms.assetid: 02d07300-e8f2-44fa-a562-5cec03af9a8c
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [XPS Documents and Packaging], GetFlags method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetFlags method, IXpsSigningOptions.GetFlags, IXpsSigningOptions::GetFlags, xps.ixpssigningoptions_getflags, xpsdigitalsignature/IXpsSigningOptions::GetFlags
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
 - IXpsSigningOptions::GetFlags
 - xpsdigitalsignature/IXpsSigningOptions::GetFlags
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
 - IXpsSigningOptions.GetFlags
---

# IXpsSigningOptions::GetFlags


## -description

Gets the <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value that specifies the signing flags to be used for this signature.

## -parameters

### -param flags [out, retval]

The <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value that specifies the signing flags to be used for this signature.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a>