---
UID: NS:msxml6.tagXHR_CERT
title: XHR_CERT (msxml6.h)
description: Defines a buffer that points to an encoded certificate.
helpviewer_keywords: ["PXHR_CERT","PXHR_CERT structure pointer [XMLHttpRequest2]","XHR_CERT","XHR_CERT structure [XMLHttpRequest2]","ixhr2.xhr_cert","msxml6/PXHR_CERT","msxml6/XHR_CERT","tagXHR_CERT"]
old-location: ixhr2\xhr_cert.htm
tech.root: ixhr2
ms.assetid: 0BBA4BDA-9A63-44A6-9B90-33B3EAE253C1
ms.date: 12/05/2018
ms.keywords: PXHR_CERT, PXHR_CERT structure pointer [XMLHttpRequest2], XHR_CERT, XHR_CERT structure [XMLHttpRequest2], ixhr2.xhr_cert, msxml6/PXHR_CERT, msxml6/XHR_CERT, tagXHR_CERT
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XHR_CERT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagXHR_CERT
 - msxml6/tagXHR_CERT
 - XHR_CERT
 - msxml6/XHR_CERT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msxml6.h
api_name:
 - XHR_CERT
---

# XHR_CERT structure


## -description

Defines a buffer that points to an encoded certificate.

## -struct-fields

### -field cbCert

 The size, in bytes, of the encoded certificate.

### -field pbCert

A pointer to the buffer that contains the encoded certificate.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest3callback-onservercertificatereceived">OnServerCertificateReceived</a>



<a href="/previous-versions/windows/desktop/ixhr2/ixmlhttprequest3-setclientcertificate">SetClientCertificate</a>