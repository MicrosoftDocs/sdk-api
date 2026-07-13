---
UID: NF:schannel.SslCrackCertificate
title: SslCrackCertificate function (schannel.h)
description: Returns an X509Certificate structure with the information contained in the specified certificate BLOB.
helpviewer_keywords: ["SslCrackCertificate","SslCrackCertificate function [Security]","schannel/SslCrackCertificate","security.sslcrackcertificate"]
old-location: security\sslcrackcertificate.htm
tech.root: security
ms.assetid: e5ffeebb-0b09-4f0a-b2dc-75fb2a3af7ed
ms.date: 12/05/2018
ms.keywords: SslCrackCertificate, SslCrackCertificate function [Security], schannel/SslCrackCertificate, security.sslcrackcertificate
req.header: schannel.h
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
req.lib: schannel.lib
req.dll: Schannel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SslCrackCertificate
 - schannel/SslCrackCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Schannel.dll
api_name:
 - SslCrackCertificate
---

# SslCrackCertificate function


## -description

<p class="CCE_Message">[The <b>SslCrackCertificate</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a> function.]

Returns an <a href="/windows/desktop/api/schannel/ns-schannel-x509certificate">X509Certificate</a> structure with the information contained in the specified certificate <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Schannel.dll.

## -parameters

### -param pbCertificate [in]

The certificate BLOB from which to create the new <a href="/windows/desktop/api/schannel/ns-schannel-x509certificate">X509Certificate</a> structure.

### -param cbCertificate [in]

The length, in bytes, of the BLOB contained in the <i>pbCertificate</i> parameter.

### -param dwFlags [in]

Set this value to <b>CF_CERT_FROM_FILE</b> to specify that the certificate BLOB contained in the <i>pbCertificate</i> parameter is from a file.

### -param ppCertificate [out]

On return, receives the address of a pointer to the <a href="/windows/desktop/api/schannel/ns-schannel-x509certificate">X509Certificate</a> structure that this function creates.

When you have finished using the <a href="/windows/desktop/api/schannel/ns-schannel-x509certificate">X509Certificate</a> structure, free it by calling <a href="/windows/desktop/api/schannel/nf-schannel-sslfreecertificate">SslFreeCertificate</a>.

## -returns

Returns nonzero if this function successfully created an <a href="/windows/desktop/api/schannel/ns-schannel-x509certificate">X509Certificate</a> structure or zero otherwise.