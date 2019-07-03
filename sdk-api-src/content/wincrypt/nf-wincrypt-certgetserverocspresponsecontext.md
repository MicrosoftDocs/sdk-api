---
UID: NF:wincrypt.CertGetServerOcspResponseContext
title: CertGetServerOcspResponseContext function (wincrypt.h)
author: windows-sdk-content
description: Retrieves a non-blocking, time valid online certificate status protocol (OCSP) response context for the specified handle.
old-location: security\certgetserverocspresponsecontext.htm
tech.root: SecCrypto
ms.assetid: 07476e43-db6b-4119-8d6b-41143b98744e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertGetServerOcspResponseContext, CertGetServerOcspResponseContext function [Security], security.certgetserverocspresponsecontext, wincrypt/CertGetServerOcspResponseContext
ms.topic: function
f1_keywords: 
 - "wincrypt/CertGetServerOcspResponseContext"
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertGetServerOcspResponseContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertGetServerOcspResponseContext function


## -description


The <b>CertGetServerOcspResponseContext</b> function retrieves a non-blocking, time valid <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) response context for the specified handle.


## -parameters




### -param hServerOcspResponse [in]

The OCSP server response handle for which to retrieve a response context. This handle is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certopenserverocspresponse">CertOpenServerOcspResponse</a> function.


### -param dwFlags [in]

This parameter is reserved for future use and must be zero.


### -param pvReserved

This parameter is reserved for future use and must be <b>NULL</b>.


## -returns



If the function succeeds, it returns a pointer to a <a href="https://docs.microsoft.com/windows/win32/api/wincrypt/ns-wincrypt-cert_server_ocsp_response_context">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure.

For a response to be time valid, the current time on the system hosting this function call must be less than the next update time for the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context. When a time valid OCSP response
is not available, this function returns <b>NULL</b> with the last error set to
CRYPT_E_REVOCATION_OFFLINE.




## -remarks



If you use the <b>CertGetServerOcspResponseContext</b> function to create multiple references to an OCSP response context, you must call <a href="https://docs.microsoft.com/windows/win32/api/wincrypt/ns-wincrypt-cert_server_ocsp_response_context">CertAddRefServerOcspResponseContext</a> to increment the reference count for the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_server_ocsp_response_context">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure. When you have finished using the structure, you must free it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreeserverocspresponsecontext">CertFreeServerOcspResponseContext</a> function.



