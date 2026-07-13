---
UID: NF:cryptdlg.GetFriendlyNameOfCertA
title: GetFriendlyNameOfCertA function (cryptdlg.h)
description: Retrieves the display name for a certificate. (ANSI)
helpviewer_keywords: ["GetFriendlyNameOfCertA", "cryptdlg/GetFriendlyNameOfCertA"]
old-location: security\getfriendlynameofcert.htm
tech.root: security
ms.assetid: a66a8573-b234-4d5d-bd38-72a3a44a0419
ms.date: 12/05/2018
ms.keywords: GetFriendlyNameOfCert, GetFriendlyNameOfCert function [Security], GetFriendlyNameOfCertA, GetFriendlyNameOfCertW, cryptdlg/GetFriendlyNameOfCert, cryptdlg/GetFriendlyNameOfCertA, cryptdlg/GetFriendlyNameOfCertW, security.getfriendlynameofcert
req.header: cryptdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFriendlyNameOfCertW (Unicode) and GetFriendlyNameOfCertA (ANSI)
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
 - GetFriendlyNameOfCertA
 - cryptdlg/GetFriendlyNameOfCertA
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
 - GetFriendlyNameOfCert
 - GetFriendlyNameOfCertA
 - GetFriendlyNameOfCertW
---

# GetFriendlyNameOfCertA function


## -description

<p class="CCE_Message">[The <b>GetFriendlyNameOfCert</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetnamestringa">CertGetNameString</a> function with the CERT_NAME_FRIENDLY_DISPLAY_TYPE flag.]

The <b>GetFriendlyNameOfCert</b> function retrieves the display name for a certificate.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters

### -param pccert [in]

A pointer to the certificate context whose display name is being retrieved.

### -param pch [out]

A pointer to a character string that receives the display name for the certificate.

### -param cch [in]

Number of characters allocated for <i>pchBuffer</i>, including the terminating <b>NULL</b> character.

## -returns

The return value is the number of characters, including the terminating <b>NULL</b> character, in the returned display name.

## -remarks

> [!NOTE]
> The cryptdlg.h header defines GetFriendlyNameOfCert as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
