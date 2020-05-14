---
UID: NE:xpsdigitalsignature.__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003
title: XPS_SIGN_FLAGS (xpsdigitalsignature.h)
description: Specifies whether markup compatibility detection must be run before signing.helpviewer_keywords: ["XPS_SIGN_FLAGS","XPS_SIGN_FLAGS enumeration [XPS Documents and Packaging]","XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY","XPS_SIGN_FLAGS_NONE","xps.xps_sign_flags","xpsdigitalsignature/XPS_SIGN_FLAGS","xpsdigitalsignature/XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY","xpsdigitalsignature/XPS_SIGN_FLAGS_NONE"]
old-location: xps\xps_sign_flags.htm
tech.root: printdocs
ms.assetid: 36fa92d4-ffd4-4666-8d3e-02436e3bb464
ms.date: 12/05/2018
ms.keywords: XPS_SIGN_FLAGS, XPS_SIGN_FLAGS enumeration [XPS Documents and Packaging], XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY, XPS_SIGN_FLAGS_NONE, xps.xps_sign_flags, xpsdigitalsignature/XPS_SIGN_FLAGS, xpsdigitalsignature/XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY, xpsdigitalsignature/XPS_SIGN_FLAGS_NONE
f1_keywords:
- xpsdigitalsignature/XPS_SIGN_FLAGS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- xpsdigitalsignature.h
api_name:
- XPS_SIGN_FLAGS
targetos: Windows
req.typenames: XPS_SIGN_FLAGS
req.redist: 
ms.custom: 19H1
---

# XPS_SIGN_FLAGS enumeration


## -description


Specifies whether markup compatibility detection must be run 
before signing.


## -enum-fields




### -field XPS_SIGN_FLAGS_NONE

The system will check for any markup compatibility elements before 
signing the package. If any markup compatibility elements are found, the signing operation 
fails with an <b>XPS_E_MARKUP_COMPATIBILITY_ELEMENTS</b> error.


### -field XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY

The system will not check for any markup compatibility elements before 
signing the package.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getflags">IXpsSigningOptions::GetFlags</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setflags">IXpsSigningOptions::SetFlags</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

