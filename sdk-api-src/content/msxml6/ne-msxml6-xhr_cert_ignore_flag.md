---
UID: NE:msxml6._XHR_CERT_IGNORE_FLAG
title: XHR_CERT_IGNORE_FLAG (msxml6.h)
description: Defines flags that you can assign to an outgoing HTTP request to ignore certain certificate errors by calling the SetProperty method on the IXMLHTTPRequest3 interface.
helpviewer_keywords: ["XHR_CERT_IGNORE_ALL_SERVER_ERRORS","XHR_CERT_IGNORE_CERT_CN_INVALID","XHR_CERT_IGNORE_CERT_DATE_INVALID","XHR_CERT_IGNORE_FLAG","XHR_CERT_IGNORE_FLAG enumeration [XMLHttpRequest2]","XHR_CERT_IGNORE_REVOCATION_FAILED","XHR_CERT_IGNORE_UNKNOWN_CA","ixhr2.xhr_cert_ignore_flag","msxml6/XHR_CERT_IGNORE_ALL_SERVER_ERRORS","msxml6/XHR_CERT_IGNORE_CERT_CN_INVALID","msxml6/XHR_CERT_IGNORE_CERT_DATE_INVALID","msxml6/XHR_CERT_IGNORE_FLAG","msxml6/XHR_CERT_IGNORE_REVOCATION_FAILED","msxml6/XHR_CERT_IGNORE_UNKNOWN_CA"]
old-location: ixhr2\xhr_cert_ignore_flag.htm
tech.root: ixhr2
ms.assetid: 22b7b3b0-a5e2-4cf1-af92-4fe66506fa40
ms.date: 12/05/2018
ms.keywords: XHR_CERT_IGNORE_ALL_SERVER_ERRORS, XHR_CERT_IGNORE_CERT_CN_INVALID, XHR_CERT_IGNORE_CERT_DATE_INVALID, XHR_CERT_IGNORE_FLAG, XHR_CERT_IGNORE_FLAG enumeration [XMLHttpRequest2], XHR_CERT_IGNORE_REVOCATION_FAILED, XHR_CERT_IGNORE_UNKNOWN_CA, ixhr2.xhr_cert_ignore_flag, msxml6/XHR_CERT_IGNORE_ALL_SERVER_ERRORS, msxml6/XHR_CERT_IGNORE_CERT_CN_INVALID, msxml6/XHR_CERT_IGNORE_CERT_DATE_INVALID, msxml6/XHR_CERT_IGNORE_FLAG, msxml6/XHR_CERT_IGNORE_REVOCATION_FAILED, msxml6/XHR_CERT_IGNORE_UNKNOWN_CA
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
req.typenames: XHR_CERT_IGNORE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XHR_CERT_IGNORE_FLAG
 - msxml6/_XHR_CERT_IGNORE_FLAG
 - XHR_CERT_IGNORE_FLAG
 - msxml6/XHR_CERT_IGNORE_FLAG
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
 - XHR_CERT_IGNORE_FLAG
---

# XHR_CERT_IGNORE_FLAG enumeration


## -description

Defines flags that you can assign to an outgoing HTTP request to ignore certain certificate errors by calling the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a> method on the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>  interface.

## -enum-fields

### -field XHR_CERT_IGNORE_REVOCATION_FAILED:0x80UL

Ignore certificate revocation errors.

### -field XHR_CERT_IGNORE_UNKNOWN_CA:0x100UL

Ignore a certificate error for an unknown or invalid certificate authority.

### -field XHR_CERT_IGNORE_CERT_CN_INVALID:0x1000UL

Ignore a certificate error caused by an invalid common name. This allows an invalid common name in a certificate where the server name specified by the app for the requested URL does not match the common name in the server certificate.

### -field XHR_CERT_IGNORE_CERT_DATE_INVALID:0x2000UL

Ignore a certificate error caused by an invalid date in the certificate. This allows certificates that are expired or not yet effective.

### -field XHR_CERT_IGNORE_ALL_SERVER_ERRORS

Ignore all server certificate errors.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>
