---
UID: NE:xpsdigitalsignature.__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003
title: "__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003"
author: windows-sdk-content
description: Specifies whether markup compatibility detection must be run before signing.
old-location: xps\xps_sign_flags.htm
old-project: printdocs
ms.assetid: 36fa92d4-ffd4-4666-8d3e-02436e3bb464
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: XPS_SIGN_FLAGS, XPS_SIGN_FLAGS enumeration [XPS Documents and Packaging], XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY, XPS_SIGN_FLAGS_NONE, __MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003, xps.xps_sign_flags, xpsdigitalsignature/XPS_SIGN_FLAGS, xpsdigitalsignature/XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY, xpsdigitalsignature/XPS_SIGN_FLAGS_NONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: XPS_SIGN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsdigitalsignature.h
api_name:
 - XPS_SIGN_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# __MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003 enumeration


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




<a href="https://msdn.microsoft.com/02d07300-e8f2-44fa-a562-5cec03af9a8c">IXpsSigningOptions::GetFlags</a>



<a href="https://msdn.microsoft.com/59467fd5-c462-4827-a4f8-e152df981ace">IXpsSigningOptions::SetFlags</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

