---
UID: NF:cryptdlg.CertViewPropertiesW
title: CertViewPropertiesW function (cryptdlg.h)
description: The CertViewProperties function displays the properties for a certificate in a user interface (UI) dialog box. This function has no associated import library. You must use the LoadLibrary and GetProcAddress functions to dynamically link to CryptDlg.dll. (Unicode)
helpviewer_keywords: ["CertViewProperties", "CertViewProperties function [Security]", "CertViewPropertiesW", "cryptdlg/CertViewProperties", "cryptdlg/CertViewPropertiesW", "security.certviewproperties"]
old-location: security\certviewproperties.htm
tech.root: security
ms.assetid: 5df840ab-fff6-4c7e-b799-51e4de4c644a
ms.date: 12/05/2018
ms.keywords: CertViewProperties, CertViewProperties function [Security], CertViewPropertiesA, CertViewPropertiesW, cryptdlg/CertViewProperties, cryptdlg/CertViewPropertiesA, cryptdlg/CertViewPropertiesW, security.certviewproperties
req.header: cryptdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertViewPropertiesW (Unicode) and CertViewPropertiesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CryptDlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertViewPropertiesW
 - cryptdlg/CertViewPropertiesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CryptDlg.dll
api_name:
 - CertViewProperties
 - CertViewPropertiesA
 - CertViewPropertiesW
---

# CertViewPropertiesW function


## -description

<p class="CCE_Message">[The <b>CertViewProperties</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext">CryptUIDlgViewContext</a> function.]

The <b>CertViewProperties</b> function displays the properties for a certificate in a user interface (UI) dialog box. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters

### -param pCertViewInfo [in]

A pointer to a <a href="/windows/desktop/api/cryptdlg/ns-cryptdlg-cert_viewproperties_struct_a">CERT_VIEWPROPERTIES_STRUCT</a> structure that contains the information about the certificate to view.

## -returns

The return value is <b>TRUE</b> if the function is successful; <b>FALSE</b> if the function fails.

## -remarks

> [!NOTE]
> The cryptdlg.h header defines CertViewProperties as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
