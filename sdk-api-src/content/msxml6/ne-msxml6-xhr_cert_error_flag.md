---
UID: NE:msxml6._XHR_CERT_ERROR_FLAG
title: XHR_CERT_ERROR_FLAG (msxml6.h)
description: Defines flags that indicate server certificate errors during SSL negotiation with the server by handling the OnServerCertificateReceived method on the IXMLHTTPRequest3Callback interface.
helpviewer_keywords: ["XHR_CERT_ERROR_ALL_SERVER_ERRORS","XHR_CERT_ERROR_CERT_CN_INVALID","XHR_CERT_ERROR_CERT_DATE_INVALID","XHR_CERT_ERROR_FLAG","XHR_CERT_ERROR_FLAG enumeration [XMLHttpRequest2]","XHR_CERT_ERROR_REVOCATION_FAILED","XHR_CERT_ERROR_UNKNOWN_CA","ixhr2.xhr_cert_error_flag","msxml6/XHR_CERT_ERROR_ALL_SERVER_ERRORS","msxml6/XHR_CERT_ERROR_CERT_CN_INVALID","msxml6/XHR_CERT_ERROR_CERT_DATE_INVALID","msxml6/XHR_CERT_ERROR_FLAG","msxml6/XHR_CERT_ERROR_REVOCATION_FAILED","msxml6/XHR_CERT_ERROR_UNKNOWN_CA"]
old-location: ixhr2\xhr_cert_error_flag.htm
tech.root: ixhr2
ms.assetid: fb7ddd8a-aa00-4ca8-9516-f16e2b8df7b4
ms.date: 12/05/2018
ms.keywords: XHR_CERT_ERROR_ALL_SERVER_ERRORS, XHR_CERT_ERROR_CERT_CN_INVALID, XHR_CERT_ERROR_CERT_DATE_INVALID, XHR_CERT_ERROR_FLAG, XHR_CERT_ERROR_FLAG enumeration [XMLHttpRequest2], XHR_CERT_ERROR_REVOCATION_FAILED, XHR_CERT_ERROR_UNKNOWN_CA, ixhr2.xhr_cert_error_flag, msxml6/XHR_CERT_ERROR_ALL_SERVER_ERRORS, msxml6/XHR_CERT_ERROR_CERT_CN_INVALID, msxml6/XHR_CERT_ERROR_CERT_DATE_INVALID, msxml6/XHR_CERT_ERROR_FLAG, msxml6/XHR_CERT_ERROR_REVOCATION_FAILED, msxml6/XHR_CERT_ERROR_UNKNOWN_CA
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
req.typenames: XHR_CERT_ERROR_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XHR_CERT_ERROR_FLAG
 - msxml6/_XHR_CERT_ERROR_FLAG
 - XHR_CERT_ERROR_FLAG
 - msxml6/XHR_CERT_ERROR_FLAG
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
 - XHR_CERT_ERROR_FLAG
---

# XHR_CERT_ERROR_FLAG enumeration


## -description

Defines flags that indicate server certificate errors during SSL negotiation with the server by handling the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest3callback-onservercertificatereceived">OnServerCertificateReceived</a> method on the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a> interface.

## -enum-fields

### -field XHR_CERT_ERROR_REVOCATION_FAILED:0x800000UL

The certificate received from the server has an invalid certificate revocation.

### -field XHR_CERT_ERROR_UNKNOWN_CA

The certificate received from the server has an unknown or invalid certificate authority.

### -field XHR_CERT_ERROR_CERT_CN_INVALID

The certificate received from the server has an invalid common name.

### -field XHR_CERT_ERROR_CERT_DATE_INVALID

The certificate received from the server has an invalid certificate date.

### -field XHR_CERT_ERROR_ALL_SERVER_ERRORS

The certificate received from the server has an invalid certificate revocation, and unknown or invalid certificate authority, an invalid common name, and an invalid certificate date.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest3callback-onservercertificatereceived">OnServerCertificateReceived</a>
