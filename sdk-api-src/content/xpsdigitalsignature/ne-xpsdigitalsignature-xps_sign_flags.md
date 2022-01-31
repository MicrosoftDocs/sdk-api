---
UID: NE:xpsdigitalsignature.__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003
title: XPS_SIGN_FLAGS (xpsdigitalsignature.h)
description: Specifies whether markup compatibility detection must be run before signing.
helpviewer_keywords: ["XPS_SIGN_FLAGS","XPS_SIGN_FLAGS enumeration [XPS Documents and Packaging]","XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY","XPS_SIGN_FLAGS_NONE","xps.xps_sign_flags","xpsdigitalsignature/XPS_SIGN_FLAGS","xpsdigitalsignature/XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY","xpsdigitalsignature/XPS_SIGN_FLAGS_NONE"]
old-location: xps\xps_sign_flags.htm
tech.root: xps
ms.assetid: 36fa92d4-ffd4-4666-8d3e-02436e3bb464
ms.date: 12/05/2018
ms.keywords: XPS_SIGN_FLAGS, XPS_SIGN_FLAGS enumeration [XPS Documents and Packaging], XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY, XPS_SIGN_FLAGS_NONE, xps.xps_sign_flags, xpsdigitalsignature/XPS_SIGN_FLAGS, xpsdigitalsignature/XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY, xpsdigitalsignature/XPS_SIGN_FLAGS_NONE
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
req.typenames: XPS_SIGN_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003
 - xpsdigitalsignature/__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003
 - XPS_SIGN_FLAGS
 - xpsdigitalsignature/XPS_SIGN_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsdigitalsignature.h
api_name:
 - XPS_SIGN_FLAGS
---

# XPS_SIGN_FLAGS enumeration


## -description

Specifies whether markup compatibility detection must be run 
before signing.

## -enum-fields

### -field XPS_SIGN_FLAGS_NONE:0

The system will check for any markup compatibility elements before 
signing the package. If any markup compatibility elements are found, the signing operation 
fails with an <b>XPS_E_MARKUP_COMPATIBILITY_ELEMENTS</b> error.

### -field XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY:0x1

The system will not check for any markup compatibility elements before 
signing the package.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getflags">IXpsSigningOptions::GetFlags</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setflags">IXpsSigningOptions::SetFlags</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>
