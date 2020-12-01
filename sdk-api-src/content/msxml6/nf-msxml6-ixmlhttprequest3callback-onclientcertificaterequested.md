---
UID: NF:msxml6.IXMLHTTPRequest3Callback.OnClientCertificateRequested
title: IXMLHTTPRequest3Callback::OnClientCertificateRequested (msxml6.h)
description: Occurs when a client receives a request for a client certificate during SSL negotiation with the server.
helpviewer_keywords: ["IXMLHTTPRequest3Callback interface [XMLHttpRequest2]","OnClientCertificateRequested method","IXMLHTTPRequest3Callback.OnClientCertificateRequested","IXMLHTTPRequest3Callback::OnClientCertificateRequested","OnClientCertificateRequested","OnClientCertificateRequested method [XMLHttpRequest2]","OnClientCertificateRequested method [XMLHttpRequest2]","IXMLHTTPRequest3Callback interface","ixhr2.ixmlhttprequest3callback_onclientcertificaterequested","msxml6/IXMLHTTPRequest3Callback::OnClientCertificateRequested"]
old-location: ixhr2\ixmlhttprequest3callback_onclientcertificaterequested.htm
tech.root: ixhr2
ms.assetid: 9c64fbb5-b755-4f1b-90f3-3cc414b3f5a4
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest3Callback interface [XMLHttpRequest2],OnClientCertificateRequested method, IXMLHTTPRequest3Callback.OnClientCertificateRequested, IXMLHTTPRequest3Callback::OnClientCertificateRequested, OnClientCertificateRequested, OnClientCertificateRequested method [XMLHttpRequest2], OnClientCertificateRequested method [XMLHttpRequest2],IXMLHTTPRequest3Callback interface, ixhr2.ixmlhttprequest3callback_onclientcertificaterequested, msxml6/IXMLHTTPRequest3Callback::OnClientCertificateRequested
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
 - IXMLHTTPRequest3Callback::OnClientCertificateRequested
 - msxml6/IXMLHTTPRequest3Callback::OnClientCertificateRequested
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
 - IXMLHTTPRequest3Callback.OnClientCertificateRequested
---

# IXMLHTTPRequest3Callback::OnClientCertificateRequested


## -description

Occurs when a client receives a request for a client certificate during SSL negotiation with the server.

## -parameters

### -param pXHR [in]

The initial HTTP request.

### -param cIssuerList [in]

The number of strings in the <i>rgpwszIssuerList</i> parameter.

### -param rgpwszIssuerList [in]

An array of strings that represent the issuer list.

## -returns

Returns <b>S_OK</b> on success.

## -remarks

<div class="alert"><b>Note</b>  This callback method must not throw exceptions.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>