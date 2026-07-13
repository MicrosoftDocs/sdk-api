---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetFlags
title: IXpsSigningOptions::SetFlags (xpsdigitalsignature.h)
description: Sets the XPS_SIGN_FLAGS value that specifies the signing flags to use for this signature.
helpviewer_keywords: ["IXpsSigningOptions interface [XPS Documents and Packaging]","SetFlags method","IXpsSigningOptions.SetFlags","IXpsSigningOptions::SetFlags","SetFlags","SetFlags method [XPS Documents and Packaging]","SetFlags method [XPS Documents and Packaging]","IXpsSigningOptions interface","xps.ixpssigningoptions_setflags","xpsdigitalsignature/IXpsSigningOptions::SetFlags"]
old-location: xps\ixpssigningoptions_setflags.htm
tech.root: xps
ms.assetid: 59467fd5-c462-4827-a4f8-e152df981ace
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetFlags method, IXpsSigningOptions.SetFlags, IXpsSigningOptions::SetFlags, SetFlags, SetFlags method [XPS Documents and Packaging], SetFlags method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setflags, xpsdigitalsignature/IXpsSigningOptions::SetFlags
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
 - IXpsSigningOptions::SetFlags
 - xpsdigitalsignature/IXpsSigningOptions::SetFlags
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
 - IXpsSigningOptions.SetFlags
---

# IXpsSigningOptions::SetFlags


## -description

Sets the <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value that specifies the signing flags to use for this signature.

## -parameters

### -param flags [in]

The <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value that specifies the signing flags to use for this signature.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a>