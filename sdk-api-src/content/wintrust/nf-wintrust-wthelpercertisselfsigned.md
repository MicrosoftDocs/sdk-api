---
UID: NF:wintrust.WTHelperCertIsSelfSigned
title: WTHelperCertIsSelfSigned function (wintrust.h)
description: Checks whether a certificate is self-signed.
helpviewer_keywords: ["WTHelperCertIsSelfSigned","WTHelperCertIsSelfSigned function [Security]","security.wthelpercertisselfsigned","wintrust/WTHelperCertIsSelfSigned"]
old-location: security\wthelpercertisselfsigned.htm
tech.root: security
ms.assetid: 456b8c8c-6ca3-469a-a415-e72109696bf5
ms.date: 12/05/2018
ms.keywords: WTHelperCertIsSelfSigned, WTHelperCertIsSelfSigned function [Security], security.wthelpercertisselfsigned, wintrust/WTHelperCertIsSelfSigned
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTHelperCertIsSelfSigned
 - wintrust/WTHelperCertIsSelfSigned
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - WTHelperCertIsSelfSigned
---

# WTHelperCertIsSelfSigned function


## -description

<p class="CCE_Message">[The <b>WTHelperCertIsSelfSigned</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperCertIsSelfSigned</b> function checks whether a certificate is self-signed. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param dwEncoding [in]

A <b>DWORD</b> value that specifies the encoding types of the certificate to check. For information about possible encoding types, see <a href="/windows/desktop/SecCrypto/certificate-and-message-encoding-types">Certificate and Message Encoding Types</a>.

### -param pCert [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure that contains information about  the certificate to check.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.