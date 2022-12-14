---
UID: NC:webservices.WS_CERTIFICATE_VALIDATION_CALLBACK
title: WS_CERTIFICATE_VALIDATION_CALLBACK (webservices.h)
description: The WS_CERTIFICATE_VALIDATION_CALLBACK callback is invoked to validate a certificate when a connection to an HTTP server has been established and headers sent.
helpviewer_keywords: ["WS_CERTIFICATE_VALIDATION_CALLBACK","WS_CERTIFICATE_VALIDATION_CALLBACK callback","WS_CERTIFICATE_VALIDATION_CALLBACK callback function [Web Services for Windows]","webservices/WS_CERTIFICATE_VALIDATION_CALLBACK","wsw.ws_certificate_validation_callback"]
old-location: wsw\ws_certificate_validation_callback.htm
tech.root: wsw
ms.assetid: 368A6162-F194-4C5C-B5FE-89633435168F
ms.date: 12/05/2018
ms.keywords: WS_CERTIFICATE_VALIDATION_CALLBACK, WS_CERTIFICATE_VALIDATION_CALLBACK callback, WS_CERTIFICATE_VALIDATION_CALLBACK callback function [Web Services for Windows], webservices/WS_CERTIFICATE_VALIDATION_CALLBACK, wsw.ws_certificate_validation_callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_CERTIFICATE_VALIDATION_CALLBACK
 - webservices/WS_CERTIFICATE_VALIDATION_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_CERTIFICATE_VALIDATION_CALLBACK
---

# WS_CERTIFICATE_VALIDATION_CALLBACK callback function


## -description

The <i>WS_CERTIFICATE_VALIDATION_CALLBACK</i> callback is invoked to validate a certificate when a connection to an HTTP server has been established and headers sent.

## -parameters

### -param certContext [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that is associated with the connection. Applications must free this structure using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>.

### -param state [in, optional]

A pointer to application specific state information. This parameter corresponds to the <b>state</b> member of the <a href="/windows/win32/api/webservices/ns-webservices-ws_certificate_validation_callback_context">WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT</a> structure.

## -returns

This callback function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The certificate validated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

If <i>WS_CERTIFICATE_VALIDATION_CALLBACK</i> returns any value other than <b>S_OK</b>, the channel will be aborted. The service proxy will also be aborted if this property was passed to <a href="/windows/desktop/api/webservices/nf-webservices-wscreateserviceproxy">WsCreateServiceProxy</a>.

The callback implementation must avoid long computation times or long blocking calls so that it returns to the caller quickly.

## -see-also

<a href="/windows/win32/api/webservices/ns-webservices-ws_certificate_validation_callback_context">WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT</a>
