---
UID: NF:msxml6.IXMLHTTPRequest3Callback.OnServerCertificateReceived
title: IXMLHTTPRequest3Callback::OnServerCertificateReceived (msxml6.h)
description: Occurs when a client receives certificate errors or a server certificate chain during SSL negotiation with the server.
helpviewer_keywords: ["IXMLHTTPRequest3Callback interface [XMLHttpRequest2]","OnServerCertificateReceived method","IXMLHTTPRequest3Callback.OnServerCertificateReceived","IXMLHTTPRequest3Callback::OnServerCertificateReceived","OnServerCertificateReceived","OnServerCertificateReceived method [XMLHttpRequest2]","OnServerCertificateReceived method [XMLHttpRequest2]","IXMLHTTPRequest3Callback interface","ixhr2.ixmlhttprequest3callback_onservercertificatereceived","msxml6/IXMLHTTPRequest3Callback::OnServerCertificateReceived"]
old-location: ixhr2\ixmlhttprequest3callback_onservercertificatereceived.htm
tech.root: ixhr2
ms.assetid: 5b00ab76-880b-4450-a6b2-fda399cc9e8b
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest3Callback interface [XMLHttpRequest2],OnServerCertificateReceived method, IXMLHTTPRequest3Callback.OnServerCertificateReceived, IXMLHTTPRequest3Callback::OnServerCertificateReceived, OnServerCertificateReceived, OnServerCertificateReceived method [XMLHttpRequest2], OnServerCertificateReceived method [XMLHttpRequest2],IXMLHTTPRequest3Callback interface, ixhr2.ixmlhttprequest3callback_onservercertificatereceived, msxml6/IXMLHTTPRequest3Callback::OnServerCertificateReceived
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
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
 - IXMLHTTPRequest3Callback::OnServerCertificateReceived
 - msxml6/IXMLHTTPRequest3Callback::OnServerCertificateReceived
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest3Callback.OnServerCertificateReceived
---

# IXMLHTTPRequest3Callback::OnServerCertificateReceived


## -description

Occurs when a client receives certificate errors or a server certificate chain during SSL negotiation with the server.

## -parameters

### -param pXHR [in]

The initial HTTP request.

### -param dwCertificateErrors [in]

The certificate errors encountered in the HTTPS connection (see XHR_CERT_ERROR_FLAG).

### -param cServerCertificateChain [in]

The number of elements in the <i>rgServerCertChain</i> parameter.

### -param rgServerCertificateChain [in]

An array of <a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cert">XHR_CERT</a> structures that represent the server certificate chain.

## -returns

Returns <b>S_OK</b> on success.

## -remarks

<div class="alert"><b>Note</b>  This callback method must not throw exceptions.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>



<a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cert">XHR_CERT</a>



<a href="/windows/desktop/api/msxml6/ne-msxml6-xhr_cert_error_flag">XHR_CERT_ERROR_FLAG</a>